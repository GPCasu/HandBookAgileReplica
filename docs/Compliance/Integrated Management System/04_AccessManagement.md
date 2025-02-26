# Access Management 

## Purpose

This instruction aims to define the criteria to be followed for the management and use of an information authentication and authorization system. It applies to all individuals involved in the processing of personal data who utilize electronic tools.

A variety of services are used in daily routines, for purposes such as development, management, marketing, etc.

The management of these services falls under the responsibility of the Internal IT department, which has centralized access control and cost monitoring.

Within the Internal IT department, the role and focus define the services for which the associated person is an administrator. For operational load balancing reasons, a service can be administered by multiple individuals.

## Access Control

Access to the electronic tools used for data processing is only allowed through the use of authentication credentials.

Service administrators are responsible for authorizing the creation, modification, and deletion of new users and their authentication credentials on the applications.

Upon formalizing authorization for the processing of personal data, each individual is assigned authentication credentials, consisting of a personal identification code (ID) and a temporary reserved password.

Those involved in data processing are responsible for managing their passwords, changing the temporary one assigned to them at the first login, and updating them periodically (every 6 months for processing exclusively personal data and every 3 months for processing sensitive data).

Authorized individuals must ensure the confidentiality of the reserved component of the credential and diligently safeguard the devices in their possession for exclusive use.

A single identification code (login) cannot be used by different individuals.

When a new service is adopted, users are added following the principle of least privilege, granting them sufficient access to perform the required work.

As with all requests within the department, onboarding activities are initiated via email to internalit@agilelab.it, containing details of the tasks to be performed.

Similarly, all additions, modifications, and deletions are supervised by the respective service administrator.

## SSO (Single Sign-On)

Whenever possible, SSO should be adopted through Azure AD integration. This allows precise access control for specific user groups.

Furthermore, user access is automatically revoked during offboarding.

In this case as well, enabling new users, which involves assigning them to the appropriate LDAP group, is the responsibility of the relevant role within the Internal IT department.

## Simple Accounts

Each individual has their own authorization profile and can only access the data they are allowed to or, for the sake of administrative management simplicity, the data allowed for the homogeneous class of the role they belong to.

These authorization profiles are configured in the appropriate security and authorization control tools used on the platforms.

Authorization profiles for each individual or homogeneous classes of individuals are identified and configured before the start of processing, limiting access to only the data necessary to perform the processing operations.

However, it is possible that some services may not offer this functionality. In such cases, internal IT members will record and manage access assignments.

All accounts must comply with the company's security standards (password security, MFA, inactivity lock).

In this situation as well, the creation of accounts and the granting of authorizations are requested from the role within the Internal IT department.

In this scenario, account removal must be performed manually as part of the offboarding procedure.

These statements must be considered when evaluating new services. During the setup and configuration of the service, the Internal IT representative will apply the most appropriate security features offered by the service. Services that do not provide an adequate level of security cannot be adopted.

At least annually, the authorization profiles of individual assignees are verified. In the event of changes to the authorization profile or new processing activities, a new appointment letter and authorization profile are provided.

## Root Accounts

Root accounts should not be limited to a single person for restoration purposes when needed; therefore, they should be used strictly for administrative activities.

Root accounts are always managed by the Internal IT department.

Shared Accounts:

Shared accounts that are not root accounts are discouraged. Exceptions must be carefully evaluated by the Internal IT department, and if approved, the reasons and individuals with access must be clearly defined. This information must be recorded and maintained in the "Shared Account Module."

## Audit

Every 6 months, the Internal IT department will review all user and administrative accounts, and discrepancies and corrective actions will be recorded.

Authentication credentials that have not been used for at least 6 months are deactivated, except those previously authorized for technical management purposes.

Credentials are also deactivated in case of loss of the quality that allows the individual access to personal data, such as in the following cases:

Termination of employment (resignation or dismissal)
Change of position
Physical account deletion is performed periodically by the information systems, usually once a year, after archiving the company's data owned by the account.

## Personnel Training and Information

In accordance with the principle of accountability, this procedure will be widely disseminated through:

Publication on the company's intranet
Presentation in company-designed training courses on the subject
Adoption and Revision of the Procedure:

This procedure takes immediate effect and will be constantly updated in light of organizational, technical, and regulatory changes in the field.

## Access Control for Clients and Potential Clients

In the absence of an AGILE LAB S.r.l. employee, the workstation should be:

In order (without any unattended documentation)
With the desktop PC turned off or locked
## Clients

Clients are only admitted to the room when an AGILE LAB S.r.l. operator is available.
Clients are identified by the AGILE LAB S.r.l. staff member who carries out the requested operations.
The AGILE LAB S.r.l. staff member manages and monitors the client throughout their stay in the room.
Furthermore:

The operations requested by the client are recorded in the application.
Clients are not admitted to the room outside of working hours.
## Considerations

Once past the entrance door, guests cannot move freely within the premises.
The access control system records the movements of various guests.
Regarding access outside working hours, it is only available for administrators.
Guests are defined as:

Guest personnel (collaborators and personnel from external companies) with continuous presence authorized to move independently (more than 2 weekly accesses)
Collaborators with occasional presence
Visitors
Authorized guest personnel who are allowed to move independently are not subject to the procedure described on the following page and must sign designations and commitments that bind them to specific rules of conduct and confidentiality.