# Infrastructure and SRE

The infrastructure/SRE team aims to design, implement and made operational infrastructure, as well as providing support for applications in production for mission critical environments.

## Roles

1. **{% role %}Services/Team Leader{% endrole %}:** is responsible for the customer and for the activities that are carried out.
2. **{% role %}Services/SRE Engineer{% endrole %}**: he is responsible for tasks, tickets and events that occur within his area of responsibility (project/customer).

## Circle

The team is organized into circles, which operate independently and are oriented to take care of the activities related to a specific customer/project.

### Team Leader

- Report to CTO and COO
- High level activities definitions
- Define and check the progress of activities
- He takes care of the organization of the team and measures its efficiency
- Organizes on-call shifts according to services and SLAs

### SRE Engineer

- Communication with the customers about status of the activities
- It is responsible for carrying out the incidents of customers assigned to the circle of members
- Writes and improves the documentation related to the circle following the standards
- Communicates problems and tensions within the circle and by the customers in stand up meetings
- Develop CI/CD pipeline and migrations
- Helps developers automate deployment
- Verifies the status of the pipelines and ensures that they are working properly
- Keeps infrastructure up to date and safe
- Keeps services operational
- Keeps backups operational
- Interfaces with HW suppliers
- Develops and maintains tools and software useful for the team following the good development practices suggested by the Software Mentor (external Role)

The **philosophy** behind this type of organization is to increase the responsibility of the team and to help the people who are part of it to have a higher level of involvement and perception of responsibility. 
In addition, everyone is responsible for something and this helps to grow every element of the team without limits of seniority.
The team has been conceived to follow the basic principles and good practices of **Site Reliability Engineering** (**SRE**).

## Team feedback loop

The team uses various tools to generate and receive feedback. 

The feedback tools are differentiated by purpose and effectiveness and are, as we read in SRE literature, used according to the type of feedback you want to give and the urgency of the event you have to manage.

An example of tools used can be mail, GitLab/Jira (e.g. Issue and task tracking), Teams and a ticket system (e.g. Jira Service Desk).

## Engagement

**External**

The times and methods of engagement are formalized by Agile Lab towards customers in terms of SLAs/SLOs/SLIs and mode of engagement (eg. ticket, email, call).
The team adapts to the needs of customers and operates in accordance with the agreements managing the interventions and the related communication in an effective and efficient manner.

**In case of strong criticality**, the engagement can / must be made by mobile phone to a member of the team and it can not refuse to manage the engagement even if busy with other activities.

## Documentation

For each project/infrastructure a technical documentation is produced that is written in markdown format and versioned through a **Git** repository ({customer}.{project}.DevOps); this documentation contains:

* an exhaustive infrastructural map of the solution (e.g. made by draw.io)
* hosts list, connection matrix, network configuration
* a detailed set of commands (command misc) to act on the various parts of the infrastructure
* backup details: storage and procedures for recovering and restoring the backup during a critical event
* HA test reports
* Postmortems

A customer agnostic project is used to contain common knowledge about services and tips&tricks. Everybody in the team is asked to contribute and keep it updated.

## Runbook

A runbook is an operational reference which is used to describe an application in a deployed environment. It should be easy to read, consistent across all services and accurate. 
This is the document an on-call responder would refer to at 3am when a P1 alert wakes him/her up, so it should be as straightforward and to-the-point as possible.
For the same reasons, it should be always up to date. Each SRE Engineer is accountable for keeping his domains runbooks up to date.

Since our team is accountable for more than a service, here we define a template that contains the main items of a runbook.

### Template

| Section | Purpose |
| ------- | ------- |
| Summary | Very short description about the functionalities/services offered |
| Service SLA | Report here ticket and service SLAs (if any) defined by contract |
| Escalation path | Useful for both the on-call team and customer |
| Incident workflow | How is an incident created and how to behave |
| Monitoring | List here all the tool used for monitoring purposes (e.g. dashboards)  |
| Alerts | For each alert, or group of alerts, describe the meaning of the metric, the impact on the customer, and possible remediation checks |
| Postmortems | Link to the postmortem collection |
| Doc | Any link to documentation that can be relevant |

## Internal tests

A stable platform is likely to live few incidents in a year, but they will fiercly suprise you when you least expect them. And at that time, we really want all our team to be ready for it.

Internal tests is the method that we enforce to assess the knowledge of the service. Aim of these trainings is to cover the following topics:

- *Process*: is it clear how to behave during an incident? How to escalate and who to engage?
- *architecture*: is it clear the purpose of each block of the application and what is its impact on the customer?
- *Troubleshooting*: here we go deep, issues are proposed in order to understand what the team member would do in that situation, what he/she would look at first and so on.  
- *monitoring*: is it clear what that alarm means? Is it documented enough?

An important aspect of internal tests is that they are particularly handy for who is approaching to jump into shifts. Moreover, they create an improvement loop whose aim is to fill the gaps emerged by the results.

Indeed, when results are ready, a meeting takes place to review the questions and create corrective actions out of it.

## Projects

Projects are defined as a sequence of activities aimed to reach a particular goal (e.g environment creation, tool development, performance optimization etc.)  
As for a software project, we adopt company [workflows and guidelines](https://publicagilefactory.gitlab.io/handbook/Workflow.html).

## Activities vs. Incidents

**Activities**

Activities can be independent tasks, or can be part of a project.

* Activities are defined with the team leader
* You can work on an activity if the related Gitlab issue has been defined
* You should only work on one activity at a time 
* Each activity is defined as follows (use related template):
  * Title, Description
  * Tasks
  * Comment feedback daily (on wip activity)
  * Deadline
  * **Definition of done**
* All activities are defined day by day using Agile methodology, which is repeated every day
* All activities/MR should be reported in the customer's repository, while generic issues/MR should be reported in the team's internal repository
* All activities/MR need to be labelled with standard tags/labels
* When activities/MR are ready, they are assigned for a review to the Team Leader

**Incidents**

* Incidents are opened and managed using a ticket system, manually or automatically generated by proactive monitoring.
* Incidents are assigned to the on-call team member or properly routed to the correct person by means of the defined escalation path.   
* **[Definition of done]** At the end of the incident, when deemed appropriate, the post-mortem and resolution documentation can be produced (see postmortem section).
* **[Definition of done]** If there is a business impact, during each phase of the incident the customers and stakeholders must be kept up to date and when it ends a report must be produced explaining what happened, actions taken and root causes

## Postmortem

A postmortem goes beyond the documentation of an incident. It represents a detailed and blameless analysis of symptoms, root cause and timeline of the event, but it is mostly about sitting down to understand what corrective actions can be taken to prevent that issue to happen again, or to modify our processes in order to better behave in such situations.

Postmortems are expected after any significant undesirable event. Writing them is a process that requires a considerable amount of time and effort, for this reason we have to choose when to write one, and there are specific triggers that help this decision:
- data loss
- on call team member intervention
- impact on the business
- monitoring failure
- recurring events

The decision to draw up a postmortem is in charge of the SRE role that has a focus on that circle, mainly based on the above mentioned triggers. With respect to all on-call team members, he/she has a broader view on incident history. General usefulness should be taken into account too, as postmortems make up a knowledge base useful for all the SRE team members when facing similar problems.

While the analysis and technical details of the incident are produced by the on-call team member, who is the only one that has a clear timeline of the events, this is just the 50% of the work.

For a postmortem to have a value, it needs to be reviewed by the team, which has to define and take charge of corrective actions.

## Joining the circle

If you want to candidate to join this circle, contact the lead link and tell him/her about it.
