
# Data Engineering 

# Overview & Motivations
This has the dual purpose of raising awareness and acting as a manifesto for all the people at Agile Lab along with our past, present, and future customers.

In the collective imagination, the Data Engineer is someone who processes and makes data available to potential consumers. It's usually considered as a role focused on achieving a very practical result: get data there - where and when it's needed.

Unfortunately, this rather short-sighted view led to big disasters in Enterprises and beyond and you know why?

**Data Engineering is a practice, not (just) a role.**

In the past, many professionals approached the "extract value from data" problem as a technological challenge, architectural at most (DWH, Data Lake, now Cloud-native SaaS based pipelines, etc …), but what has always been missing there is the awareness that Data Engineering is a practice, that as such needs to be studied, nurtured, built and disseminated.

We have always dissociated ourselves from this too simplistic vision of Data Engineering, conscious of possible misunderstanding by the market when expecting from us such kind of "basic service". We'd like to state this once again: **Data Engineering is not about moving data from one place to another, or executing a set of queries quickly (thanks to some technological help), or even "supporting data scientists". Data Engineering, as the word says, is *engineering the data management practice*.**

When we talk about Engineering, in a broader viewpoint, we aim precisely to this: designing detailed and challenged architectures, adopting methodologies, processes, best practices, and tools to craft reliable, maintainable, evolvable, reusable products and services that meet the needs of our society.

Would you walk over a bridge made of some wooden planks (over and over again, maybe to bring your kids to school)?

Now, we don't understand why some people talk about Data Engineering when, instead, they refer to just creating some data or implementing ETL/ELT jobs. It's like talking about Bridge Engineering while referring to putting some wooden planks between two pillars: here the wooden planks are the ETL/ELT processes connecting the data flows between two systems. Is this really how would you support an allegedly data-driven company?


**Now let's talk about data and how we manage it**

Data is becoming the nervous system of every company, large or small, a fundamental element to differentiate on the market in terms of services offer and automated support to business decisions.
If we genuinely believe that they are such a backbone, we must treat them "professionally"; if we really consider them a good, a service, or a product, we must engineer them. There is no such thing as a successful product that has not been properly engineered. The factory producing such products has undoubtedly been super-engineered to ensure low production costs along with no manufacturing defects and high sustainability.

**We believe that data is crucial, and we assume that this is just as true for our customers.**

That's why we've been trying to engineer the data production and delivery process for years from a design, operation, methodology, and tooling perspective. Engineering the factory but not the product, or vice versa, definitely leads to failure in the real world. It is important to engineer the data production lifecycle and the data itself as a digital good, product, and service. Data does not have only one connotation, instead it is naturally fickle. It is a system that must stay balanced because, exactly as in quantum systems, the reality of data is not objective but depends on the observer.

Our approach has always been to consider the data as the software (and in part, the data is software), but without forgetting the greater gravity (Data Gravity - in the Clouds - Data Gravitas).

**We envision a world where top-notch Data Engineers make the difference for the success of a data-centric initiative.**

Data teams will be more accountable for business outcomes, they'll have to work to the best of their ability to make sure their products are maintainable and evolvable over time. Their outcomes and quality will be measurable, objectively. It will be straightforward to differentiate teams working with high-quality standards from those performing poorly, and we sincerely look forward to this.

Too many data engineers focus on tools and frameworks, but practices, concepts, and patterns matter even more. In fact, **all technologies will inevitably become obsolete at some point, while good organizational, methodological, and engineering practices can last a long time.**

Our Data Engineering pratice is not focusing only on data. Still, it guarantees that the data will be of high quality, that it will be easy to find and correct errors, that it will be simple and inexpensive to maintain and evolve, and that it will be safe and straightforward to consume and to understand.
It's about practice, data culture, design patterns, broader sensitivity across many more aspects we might be used to when "just dealing with software". At Agile Lab, we invest every single day in continuous internal training and mentoring on this, because we believe that our Data Engineering practice will be the a key success factor for our customers.






Time to show the cards.

So let's come to what we think are the characteristics and practices that should be part of a good Data Engineering process.



# Data Processing

### Software Quality:
The software producing and managing data must be high-quality, maintainable, evolvable. There's no big difference between software implementing a data pipeline and a microservice in terms of quality standards! In terms of workflow, ours is public and open source. You can find it [here](./Workflow.md)
Software design patterns and principles must also be applied to data pipelines development. Please stop scripting data pipelines (notebooks didn't help here).

### Decoupling:
It has become a mantra in software systems to have well-decoupled components that are independently testable and reusable.
We use the same measures with different facets in data platforms and data pipelines.

A data pipeline must:
- Have a single responsibility and a single owner of its business logic.
- Be self-consistent in terms of scheduling and execution environment.
- Be decoupled from the underlying storage system.
- I/O actions must be decoupled from business (data transformation) logic, so to facilitate testability and architectural evolutions.

Also, it is essential to have well-decoupled layers at the platform level, especially storage and computing.

### Reproducibility:
We need to be able to re-run data pipelines in case of crashes, bugs, and other critical situations, without generating side effects. In the software world, corner case management is fundamental, just like (or even more) in the data one (because of gravity).

We design all data pipelines based on the principles of immutability and idempotence. Despite the technology, you should always be in the position to:
- Re-execute a pipeline gone wrong.
- Re-execute an hotfixed/patched pipeline to overwrite the last run, even if it was successful.
- Restore a previous version of the data.
- Run a pipeline in recovery mode if you need to clean up an inconsistent situation. The pipeline itself holds the cleaning logic, not another job.

So far, we have talked about data itself, but an even more critical aspect is the reproducibility of the underlying environments and platforms status. 
Being able to (re)create an execution environment with no or minimal effort, drastically simplifies tasks such as on-the-fly tests, environment migrations, platform upgrades or simulating disaster recovery. It would also reduce the need of regression tests on large amounts of data.
It's an aspect to be taken care of and that can be addressed through IaC and architectural Blueprint methodologies.


### Performance:
Performance and scalability are two engineering factors that are critical in every data-driven environment. In complex architectures, there can be hundreds of aspects with an impact on scalability and good data engineers should possess them as foundational design principles.
Once again, it is important to highlight the importance of a methodological approach. There are several best practices to encourage:

* Always isolate the various read, compute, and write phases by running dedicated tests that will point out specific bottlenecks thus allowing better-targeted optimization: when you're asked to reduce the execution time of a pipeline by 10%, it must be clear which part of the process is worth working on. A warning here: isolating the various phases brings up the theme of decoupling and single responsibility. If your software design doesn't respect these principles, it won't be modular enough to allow clear steps isolation. For example, Spark has a lazy execution model where it is very hard to discern read times from transformation and write times if you are not prepared to do so.

* Always run several tests on each phase with different (magnitudes of) data volumes and computing resources to extract scaling curves that will allow you to make reasonable projections when the reference scenario will change: it's always unpleasant to find out that input data is doubling in a week and we have got no idea of how many resources will be needed to scale up. In pipeline performance tests, the worst case scenario should be designed with a long-term data strategy in mind.




# Data Documentation:

Documentation and metadata should follow the same lifecycle of code and data. Computational governance policies of the data platform should prevent new data initiatives to be brought into production if not well paired with the proper level of documentation and metadata. This is foundation for having good data products that are genuinely self-describing and understandable.
Having ex-post metadata creation and publishing can introduce a built-in technical debt ( data-debt) due to the potential misalignment with the actual data already available to consumers. It's then good practice to make sure that metadata resides within the same repositories of pipelines' code generating the data, which should imply synchronization between code and metadata and ownership by the very same team. For this reason, metadata authoring shouldn't take place on Data Catalogs, which are supposed to help consumers find out the information they need. Embedding a metadata IDE to cover malpractices in metadata management won't help in cultivating this culture.

When we implement metadata is important to rely on open standards and don't re-invent the wheel.




# Data Versioning:

The observability and reproducibility issues are rooted in the ability to move nimbly on data from different environments as well as from different versions in the same environment (e.g., rollback a terminated pipeline with inconsistent data).

Data, just like software, must be versioned and portable with minimum effort from one environment to another.

Many tools can help (such as LakeFS), but when they are not available it's still possible to set up a minimum set of features allowing you to efficiently:
- Run a pipeline over an old version of data (e.g., for repairing or testing purposes)
- Make an old version of the data available in another environment.
- Restore an old version of the data to replace the current version.

It is critical to design these mechanisms from day zero because they can also impact other pillars.




# Data Security:

It is part of an engineer's duties to take care of security, in general. In this case, data security is becoming a more and more important topic and must be approached with a by-design logic.

It's essential to look for vulnerabilities in your data and do it in an automated and structured way so to discover sensitive data before they go accidentally live.

This topic is very important at Agile Lab, so much that we have even developed proprietary tools to promptly find out if sensitive information is present in the data we are managing. These checks are continuously active, just like Observability checks.

Data Security at rest:
Fine-grained authentication and authorization mechanisms must exist to prevent unwanted access to (even just portion of) data (see RBAC, ABAC, Column and Row filters, etc…).

Data must be protected, and processing pipelines are just like any other consumer/producer so policies must be applied to storage and (application) users, that's also why decoupling is so important.

Sometimes, due to strict regulation and compliance policies, it's not possible to access fine-grained datasets, although aggregates or statistical calculations might still be needed. In this scenario, Privacy-Preserving Data Mining (PPDM) comes in handy. Any well-engineered data pipeline should compute its KPIs with the lowest possible privileges to avoid leaks and privacy violations (auditing arrives suddenly and when you don't expect it). Have fun the moment you need to ex-post troubleshoot a pipeline that embeds PPDM, which basically gives you no data context to start from!




# Data Review:

Just as code reviews are a good practice, a good data team should perform and document data reviews. These are carried out at different development stages and cover multiple aspects such as:
- Documentation completeness
- Semantic and syntactic correctness
- Security and compliance
- Data completeness
- Performance / Scalability
- Reproducibility and related principles
- Test cases analysis and monitoring (data observability)

We encourage adopting an integrated approach across code base, data versioning, and data issues.




# Data Testing and Observability:

Testing and monitoring must be applied to data, as well as to software, because static test cases on artifact data are just not enough. We do this by embracing the principles of DODD ([Kensu | DODD](https://www.kensu.io/dodd)). Data testing means considering the environment and the context where data lives and is observed. Remember that data offers different realities depending on when and where it's evaluated, so it's important to apply principles of continuous monitoring to all the lifecycle stages, from development through deployment, not only to the production environment.

When we need to debug or troubleshoot software we always try to have the deepest possible context. IDEs or various monitoring and debugging tools help by automatically providing the execution context (stack trace, logs, variables status, etc.) letting us to understand the system's state at that point in time.

How often did you see "wrong data" in a table having no idea on how it got there? How exhausting was finding the piece of code allegedly generating such data (hoping it's versioned and not hardcoded somewhere), trying to mentally re-create the corner case that might have caused the error, searching for unit tests supposedly covering such corner case, scraping the documentation hoping to find references of that scenario… It's frustrating, because data seems just plunged from the sky, with no traces left. Probably 99% of data pipelines implemented out there have no links between the input (data), the function (software) and the output (data) thus making troubleshooting or, even worse, the discovery of an error just a nightmare.

In Agile Lab, we apply the same principles seen for software: we always try to have as much context as possible to understand better what's happening to a specific data row or column. We try to set up lineage information (stacktrace), data profiling (general context) and data quality before and after the transformations we apply (execution context). All these information need to be usable right when needed and be well organized.


This practice is about people - professionals - not tools. Of course, many tools help in implementing the practice, but without the right mindsets and skills they are just useless.


Keep in mind that ex-post checks don't solve quality problems because consumers in the mean time probably already ingested faulty data (remember the data gravity thing?) and they don't provide any clues about where and why the errors came up. This to say that it makes a huge difference **to proactively anticipate checks and monitoring so to make them synchronous with the data generation** (and part of applications-generating-data lifecycle).




# Data Issues:

As seen in previous section, Data Observability provides capabilities to perform root cause analysis, but how do we document the issues? How do we behave when a data incident occurs? The last thing you want to do is to "patch the data"; what you need to do is fixing the pipelines (applications), which will then fix the data.
First, the data issues should be reported just like any other software bug. They must be documented accurately, associating them with all the contextual information we extracted from the data observability, to clarify what would have been expected, what happened instead, what tests have been prepared and why they did not intercept the problem.
It is vital to understand the corrective actions at the application level (they could drive automatic remediation) as well as the additional tests that need to be implemented to cover the issue.
Another aspect to consider is the ability to associate data issues to the specific version of both software and data (data versioning) responsible of the issue because, sometimes, it's necessary to put in place workarounds to restore business functionality first. At the same time, while data and software evolve independently, we must reproduce the problem and fix it.
Finally, to avoid repeating the same mistakes, it's crucial to conduct a post-mortem with the team and ensure these are saved in a simil-wiki or somehow associated with the issue, searchable and discoverable.




# Data Interoperability:

We believe data should be easily accessible across the organization, there should not be barriers for data consumers to interact with data ( except security and authorization constrains). This high availability must also be paired with low coupling between who produces and exposes the data and who consumes it. 

The first aspect are metadata, when we expose data they must be paired with **data contracts** and **data sharing agreements**.

**Data Contracts** should be a standard way to describe the data and the terms of the offered service. Let's consider data as a service we offer to the organization. Terms of service should include SLO and SLA and how people can use the data we are offering ( for example only for development or testing purposes ).
SLO and SLA instead should describe what level of quality we want to reach or we guarantee, also uptime, data downtime, timeliness, refresh rate should be described. 
Data Contracts should follow the same life cycle of metadata and documentation see section "Data Documentation", but in the end they should be available to everybody in the organization ( no sensitive data here ) in a human and machine readable format, because they have a big role in decoupling data processing from data storage across domains or different stakeholders.

**Data Sharing Agreements** are an extension of Data Contracts and are more focusing on what is the intended usage, privacy and purpose ( including limitations ). For example, they should make clear if data filters will be applied for governance and security purposes or if some data life cycle policy is in place ( data deletion or data retention ). Data Sharing Agreements can be global or also specific for some set of consumers, but they need to be clear and understandable. They also follow the "Data Documentation" process, but they only need to be human readable. In any case, they are an important aspect for data interoperability, because they increase the consumer awareness.

When focusing on the technical and physical aspects instead, we need to take care of how we expose the data. These are key aspects we need to keep in consideration to boost the interoperability:
* Data is consumable from a single API/Interface/Connector and there is no need to integrate with several technologies to consume different data sets across the organization.
* Data is consumable for different needs ( data exploration, dashboarding/reporting, data intensive processing ). When we expose data we don't overfit on a use case and we keep the door open for new use cases.
* The consumer doesn't need to know the physical location of the data, because this is going to generate high coupling between producer and consumer. We want them to discover the physical location at runtime ( pre-flight pattern ) or otherwise refer to logical locations.
* Data is exposed through open standards and protocols. They will facilitate the consumer to read the data with a multitude of tools and methods. This is also interoperability. "Open" means that there is a specification and then everybody can implement and extend it, but also that there is an ecosystem of tools adopting it. Open but not used in the industry is not enough.




