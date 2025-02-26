
# Estimation and Planning

During the pre-sale of a project, an effort estimation is always due to be able to correctly price the project.
Price is a direct consequence of the amount of "days" that can be used to carry out the project. 

However, at the beginning of each project, a second estimate will be done, and it will be in charge of the Project Leader and reviewed by the COO for acceptance. Based on this estimate (which may differ from the first, if accepted by the COO) and the relative project planning, the right team with the needed skills will be allocated.

Every single project or product, should fit inside the general capacity plan that is managed by the COO, in order to be always sure to be able to deliver everything.


# Capacity Plan

In order to improve the *alignment* of people with the strategy of the company, the COO will periodically publish the updated capacity plan in the Sharepoint "BigData" / "Capacity Plan".
Capacity Plan can help people in understanding:

* their own priorities and allocations, improving their level of autonomy.
* overall people allocation and teams composition
* which projects are in pipe

Anyway this document is not "reactive", then allocations may change in case of emergencies or contingencies, and everyone is empowered to propose modifications for its own allocation in case he feels it is not reflecting the real needs and priorities of the company.

Keep in mind that capacity plan is not always precise in every details and very often when projects are still in proposal phase, you will find hypothetical allocations that could change week by week. The only allocation that is 100% sure is the one related to a project that is already started.

Here the legend to comprehend the document.
- Project: Name of the project or sub-project
- Team: members involved in the activity
- Allocation: default allocation for each team member (this is a technical column, not relevant for the reader)
- Capacity x unit: number of MD ( man days ) allocated for a specific team member
- Capacity Requested: total estimation of MD for the project
- Capacity Tot: total amount of allocated MD

Then you have the allocation percentage of each team member on a bi-weekly base. This is the important factor to be autonomous in allocating activities properly. 

# Team Organization

Each project or product will be a circle in which the following roles may be present:

*   Project Leader - mandatory
*   Developer - mandatory
*   Architect - mandatory
*   Devops - optional
*   PMO - optional
*   Account - optional

# Project lifecycle

The project lifecycle is really dependent on how a customer uses to run a project.
<br/>We work with customers adopting scrum, scaled agile frameworks, waterfall and anything in the middle.
<br/>Thus, we adapt to customers processes and practices.

Nevertheless, whenever we detect ways to bring values through our agile methodology, we keep proposing activities, practices and improvements.

<br/>We monitor the project quality looking into different dimensions: [Software Quality](ProjectSoftwarePractices.md) and Customer Satisfaction.
<br/>The Software Quality provides insights about what we are really doing and how.
<br/>The Customer Satisfaction is about a customer feels about our contributions (development, leadership, communication, speed).
<br/>They are both important and we care to do our best in the two directions.

For internal projects, we adhere to our [Software Development Lifecycle](SoftwareDevelopment.md).

We also categorize projects in two types:
- **Formal**: the customer requires an end to end solution released in production and with full visibility on deliverables. Customer also produces detailed requirements and both functional and technical analysis are required.
- **Informal**: requirements are leaking, we have to deliver quick win to the customer and the process is clearly iterative.

While working within a project, regardless the project style, we care about the whole lifecycle from requirements to deployment and maintenance:
*   Design
*   Implementation
*   Validation
*   Deployment  


## Design

The Design phase of a project (or iteration) involves Project Leader and Architect, and optionally - but recommended - Developers (at the discretion of the Project Leader).
The deliverables at this stage are:
- High-Level Design ([HLD](HLD.md))
- Functional Analysis (If the complexity of the problem requires it and we are in the context of a Formal project, this tends to be provided by the customer and validated by the project team)
- Low-Level Design (LLD)

Project Lead and Architect assigned to a project define the [HLD](HLD.md) document taking into account the following factors:
- Functional requirements of the project
- Possibly pre-existing architecture 
- The client's ability to exercise the new architecture (in case Agile Lab is not in charge of the run and maintenance service)
- Deployment Technical Constraints
- Agile Lab Technical Strategy
- Skill of the team that composes the project circle

The HLD is the starting point for discussion and alignment with the development team, and it is an accountability of the Architect.
The HLD should go into the following topics (all that apply):
- Logical architecture
- Physical architecture
- Software architecture
- High-level data flow
- Integrations
- Performance analysis

The development team goes into the Low-Level Design, where several aspects are taken into account: logical flow, error handling, interface sketch, logging, patterns, prototyping and all is necessary to comply with customer requirements and project constraints.

For internal projects (or whenever a customer is not ready to manage a backlog or plan), the LLD must be implemented in the form of Issue GitLab to form the project backlog, which will then be iteratively refined throughout the project. Issues can also be integrated with documents, schemas, and everything the development team thinks is necessary to make each development task understandable.

At this stage, it is also necessary to involve the Developer Productivity Ninja who will indicate which software components already developed in the past should be reused or can provide indications on which components could become an asset for the future.

The LLD must then be shared with the Architect and Project Leader and approved by them.

At this point, there are conditions to start the development. HLD/LLD iterations may be shorter or longer depending on the project.

## Implementation

This phase may be visible or nor to the customer depending on the kind of commitment established.
<br/>Whenever necessary, the software development lifecycle adapts to the customer development practices.
<br/>We strive for opportunity to better dev practices and so we feel free to propose improvements to the customer or consider to refactor our development lifecycle if there are good experiences to bring in(see [Software Development](SoftwareDevelopment.md)).

From an operations standpoint we enforce three type of controls along the project lifecycle:

#### Delivery Control
The circle Engine is the space where Project Leaders and Business Unit Leads can share project status and updates with the COO (Delivery Leader) through tactical meetings. 
<br/>Project/Business Unit Leads are encouraged to give timely feedbacks anyway.

For projects traced internally, Gitlab must always be updated and provide all the necessary details about the status of a project. 

Every three weeks, however, there will be a governance meeting within the circle Engine where any organizational issues within the various projects will be discussed, including resource staffing.

The Project Leader within her/his circle is free to organize the work and coordination methods that she/he considers the most appropriate and for this reason no further details will be defined on this matter, as stated in the handbook regarding the circle's properties. 

Formal projects may require the PMO to maintain higher-level project plan and manage the communication flow with the customer. 

#### Technical Control

At the beginning of each project, an "Architect" is assigned to agree on system architecture and technologies that will be used, so that customer expectations and technological consistency will be preserved.

Along with the implementation phase, the Project Leader is responsible for the quality of the code and all the technical detail choices that arise on a daily basis, this is done through a system of code review and feedback.
Each member of the development team should be proactive in solving problems and sharing solutions with the Project Leader and Architect as it pertains to them.
If the choices to be made represent a change or introduce new aspects to the system from an architectural standpoint, it will be necessary to align the Architect and also produce a new version of HLD. 

Each team member must be respectful of the organization and the Project Leader's decisions, helping him or her maintain leadership and taking care of the team's success. 
If the Project Leader does not have enough technical leadership to make good decisions, they can use the support of the Architect and consult the Software Factory circle.
Software Factory cares about best practices and guidelines, it is not in charge of specific developments and cannot decide disruptive changes. If the proposed solution changes the behavior of the system, a comparison with the Architect is therefore required.

This circle Software Factory may require to have in-depth sessions with the project team and/or participate in the code review phases with individuals.

It is very important to distinguish between "system" and "implementation" aspects, software developers can suggest system solutions (as well as others that participate in informal meetings or brainstorming sessions), but these must always be reported and validated by the Architect to be sure to take decisions with the appropriate context and vision.

#### Financial Control

The costs of Agile Lab projects are kept under control with a budgeting tool: Elapseit.
Company staff will need to fill out allocation timesheets directly on this tool at least on a weekly basis, to allow appropriate cost tracking and reporting.


#### Strategic Control

Project Leads are key people in a project. They are asked to gain context and apply the strategic vision of Agile Lab.

A Project Lead sets all the necessary meetings and project artifacts to keep information, communication, decision-making traced and functioning.

Macro-plans, strategic meetings, partnership with and sponsorship by our customers are activity to nurture and care about.

Periodically, Customer Account and Project Lead should align each other on the following items: 
*   Actual importance of the customer for Agile Lab
*   Prospective importance of the customer for Agile Lab
*   Where the project is located in the overall customer strategy
*   What topics or projects will be pushed to the customer in the next months
*   What aspects or dynamics should be seized by the project leader
