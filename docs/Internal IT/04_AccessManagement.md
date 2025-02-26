# Access Control

Services can be used by a number of employee, requiring different level of authorizations. Some of them are used for business critical purposes, thus requiring more strict rules and auditing features. 

For this reason, Internal IT is also responsible to guarantee services compliance from an access control standpoint.

In this document we define the access management guidelines adopted by Internal IT. 

### Guidelines

- Each user is provided temporary credentials that she/he will change at first login and periodically refresh.
- Credentials are provided using the least privilege principle
- Credentials should always be associated to a single person. Exceptions need to be motivated and evaluated.
- The strongest security features permitted by the service will be enforced
- Services that do not offer strong enough security features for the needed use case are discarded

#### SSO
Whenever possible, SSO is the preferred way to go: this is the easiest way to manage onboarding and offboarding, as well as a central credential management.

#### Simple accounts

When sso is not an option, single accounts are created by Internal IT for each user, enabling all security features allowed by the service.
Internal IT manages the lifecycle of the accounts, which includes permissions modifications, or its deletion.
These accounts are periodically checked.

#### Root account

Each service usually has a root account, which is managed by Internal IT and used only when strictly necessary.

#### Shared accounts

Usually forbidden for audit purposes. Exceptions need to be motivated and carefully evaluated by Internal IT.