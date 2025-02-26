# Software Design Guidelines

This section lists guidelines and best practices related to software design at any scale, from classes and methods up to monolithic or distributed applications.

## Package design

*Premise: while Java and Scala have 'packages' as an explicit programming construct, you can generalize the following guidelines to other languages by applying them to 'folders', 'namespaces', or whatever construct that allows you to group files/classes.*

The package structure of an application is a key factor in determining the maintainability and understandability of the codebase,
and eventually in ensuring a good developer experience.

Packages are not simply a way to group classes. They should be considered as units of encapsulation and important architectural constructs.
As such, they obey to the same principles of high-cohesion and low-coupling that apply to any scale in software. 

Even more important, **a package is a modelling construct** and should be used to express the key concepts of the domain.

### Guidelines

**Each package should model a feature**

In short, a feature is a concept. It can be a domain concept, such as:  an entity of domain, an operation or a whole use-case.

*Ex.: user (entity), changePassword (use case), checkPasswordValidity (operation).*

While your primary concern should always be the modelling of business logic, since software is made up of infrastructure too, a feature can also be an infrastructure concept.

*Ex.: ‘database.connection’, ‘http.server’.*

**Prefer packaging by feature to packaging by type or by layer**

Grouping together classes that does not collaborate while simply share some technical aspect (i.e.: they have a common super-type or belong to the same architectural layer) is discouraged.

*Ex.: having a ‘exceptions’ package is meaningless: exceptions’ are not a feature, but simply a programming construct.*

Similarly,  in a MVC architecture you should avoid having ‘controllers’, ‘views’ and ‘models’ packages, since they are not features either.
Although several frameworks suggest (or even mandate) this kind of organisation, it has several drawbacks, because it spreads all classes related to a single feature in distinct places. Moreover, such packages naturally become bigger over time, so this approach does not scale.

A package should not necessarily match a single layer. A package should instead contain all classes related to a given feature.

*Ex. a `login` or `user.login` package should contain UserController, User, LoginService, LoginResult, LoginException and so on.*

As you can see, several classes having different types or belonging to different layers are put in the same package (Controller, Exception …) since they collaborate to realise the same feature.
This allows to easily detect, understand and modify that feature in one place. 

At the same time you can maintain the layer separation at a class level (i.e. having distinct classes for Controller, Service etc…) to guaranteeing separation of concerns and testability.

**Try to avoid `common` or `utils` packages**

You should avoid having a giant `common` package containing all sort of classes such as DatesUtils, ParsingUtils etc.  
Such a package does not convey any useful information. 

Use distinct feature-oriented packages instead, such as `parsing`, `date`, that are more expressive.

**Group features in package-groups**

As the application grows it raises the need to group features to get a clear and organised architecture.  
To this purpose you can group several related packages under one parent package, that we'll call a 'package-group'.

A package-group does not represent a feature int itself, but just a way to group related features.

*Ex.: create a `user` package-group that contains all user-related features such as `user.login`, `user.changepassword`, `user.logout` sub-packages.*

**Make packages cohesive and low coupled**

Classes that belongs to the same package should be tightly coupled: they are typically used together to perform some action,
cannot be reused independently and tend to be modified together. This makes the package ‘cohesive’.
When packages are highly cohesive they also tend to be low coupled (even if not always).

A useful trick to raise cohesion: **use method signatures as a guide** to find classes and types that work together.  
Also consider to extract the common logic between two features in a separate feature.

*Ex.: UserController, User, LoginService are collaborating classes that work together to perform a use case. 
So you decide to put them in the package `user.login`.  
Now suppose that LoginService has the following method: login(val credentials: Credentials): LoginResult;  
In this case you should consider moving also Credentials and LoginResult in the `user.login` package (making it choesive).
Now `user.login` and `user.logout` can be independently developed (low coupled): each has its own controller, view and so on.
However they share the User class, so you can decide to move it to the `user` package.*

**Create a root package and a config package**

The suggested structure for your application is the following:

```
.
└── it.agilelab.myproject-group.myproject.app
	├── config
	├── features
	├── infrastructure
	AppMain.class
```

where
- `config` contains all configuration related code, for dependency injection. 
`config` depends on all other packages, while no package should depend on `config`.
- `features` and `infrastructure` are package-groups
- AppMain is a class containing the ‘main’ 

