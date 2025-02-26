# Customer Support

### Purpose

Provides assistance to customers post-purchase, ensuring they can effectively use the software and resolve any issues that arise.

### Support Workflow

Witboost does not rely on 3rd-parties to deliver professional, educational nor product support services to our customers either. All support services are provided by Witboost employees from Europe.

![Support Workflow](/images/product%20processes/SupportWorkflow.png)

For Witboost, the support workflow is managed on Jira with dedicated boards for each customer. The support team is responsible for managing the tickets and ensuring that they are resolved within the agreed-upon SLA. The customers can see the status of their tickets and communicate with the support team through the Jira platform.

#### Problem Identification
Problem identification means the notification of a problem. The problem should be understood in the best way possible before work can start to fix it. Problems are generally identified in one of two ways: either through a Jira ticket opening from an end-user, or the end-user can ask the Professional Services team to handle the ticket for them.

#### Ticket Creation
When creating a ticket on Jira, the problem should be described in detail to be analyzed and solved.

Usually, a Jira ticket contains the following details:
- A name that represents the error;
- The description, that should contain the overall problem: how to reproduce it, what kind of limitations are related to it, what is the expected behavior, etc;
- Impact of the problem (extensive, significant, moderate, etc);
- Urgency of the ticket as perceived by the customer;
- Affected Witboost version and components.

After the ticket has been taken into charge, the ticket status will be updated by the support team, along with:
- Comments, questions, and notes;
- Resolution details;
- Link to other similar tickets.

#### Categorization
Ticket categorization helps routing to the right resolution team and saves much time in troubleshooting.

The reporter opens a ticket with a specific type, chosen among:

<table>
  <tr style="background-color: black; color: white;">
    <th>Ticket Type</th>
    <th>Description</th>
  </tr>
  <tr style="background-color: #d3d3d3; color:black;">
    <td>Incident</td>
    <td>Impacts heavily the functionalities of Witboost: i.e. users are no able to use any of the major functionalities
    </td>
  </tr>
  <tr style="background-color: #a9a9a9; color:black;">
    <td>Bug report</td>
    <td>There are one or more problems while performing some operations, that do not prevent users from using Witboost
    </td>
  </tr>
  <tr style="background-color: #d3d3d3; color:black;">
    <td>Get IT help</td>
    <td>Questions, improvements, new features, etc.
    </td>
  </tr>
</table>

After the ticket is opened, the support team proceeds with the categorization (optionally by changing its type) and adds relevant details.

#### Prioritization
The support team determines the ticket's priority based on the urgency and priority specified by the ticket reporter and assesses its overall impact. This impact is generally aligned with the fault's severity, which is evaluated by considering factors such as service downtime, the number of users affected, and the frequency of the issue, among others.

Below is a summary table of prioritization, taking into account impact and urgency:

![Prioritization Workflow](/images/product%20processes/PrioritizationImpact.png)

#### Investigation & Diagnosis
The diagnosis step is crucial for identifying and understanding the problem.

This step involves collecting all relevant information about the incident and this may include log records, monitoring data, user reports and all other pertinent information.
To avoid time-consuming conversations, the ticket should contain all the evidence and tests the reporter performs; in case of missing information, the support team will ask for it to the customers, but this could lead to a delay in the resolution.
All activities carried out are tracked directly on the Jira ticket. This provides feedback to the customer on ongoing activities and is needed to align other team members on what has been done and/or discovered.

#### Escalation
If the diagnostic step does not lead to an immediate resolution or if the ticket requires additional resources or expertise, an escalation is performed.
Escalation involves escalating the incident to a higher level of support or a specialized team for more advanced resolution.

#### Resolution & Recovery
Resolution and recovery are performed once the problem is fully understood. Finding a resolution to an incident means that a way of rectifying the issue has been identified. The ticket’s assignee will be responsible of communicating how the resolution will be delivered to the customer: e. g. configuration changes or the release of a new patched version.

#### Closure
After completing the steps outlined above, the ticket can be considered resolved and closed.

A follow-up with the customer is conducted to ensure that the resolution is satisfactory, and if confirmed, a patch release is issued in case the problem is related to a bug.

The workflow is outlined below:

![Jira Ticket Workflow](/images/product%20processes/JiraTicketWorkflow.png)

### Service Level Agreements

The Service Level Agreement (SLA) is a formal contract between Witboost and a customer that defines the specific level of service expected, including measurable performance indicators such as response times, resolution times and availability standards.

The SLA outlines the responsibilities of both parties, sets expectations for service delivery and details what happens if these expectations are not met, often including penalties or compensations.

The activities and features that are included in the Subscription Fee are:
- Product components features: non-exclusive and free license for the period during which the subscription shall be provided for all Witboost’s IP components (first release)
- Evolutionary features: non-exclusive and free license for the period during which the Subscription shall be provided (Witboost’s IP components additional releases)
- Second-level support ticketing service (via Jira ticketing service). This support is provided 8 hours per day, 5 day per week from 9 a.m - 1 p.m and 2 p.m - 6 p.m CET/CEST
- Corrective maintenance (bug fixing)
- Updates service (to adapt for instance to infrastructure major changes)

The perimeter of all the services is the Witboost IP Components (templates and plug-ins are excluded).

Only for **incidents** and **bugs**, the response and resolution times are defined in every contract, based on priority, as outlined in the table below:

<table>
  <tr style="background-color: black; color: white;">
    <th>Level</th>
    <th>Description</th>
    <th>SLA</th>
  </tr>
  <tr style="background-color: #d3d3d3; color:black;">
    <td>P1 - Critical</td>
    <td>Taking charge of blocking tickets</td>
    <td>within 1 hour</td>
  </tr>
  <tr style="background-color: #a9a9a9; color:black;">
    <td>P1 - Critical</td>
    <td>Update</td>
    <td>every 4 hours</td>
  </tr>
  <tr style="background-color: #d3d3d3; color:black;">
    <td>P2 - Serious</td>
    <td>Taking charge of non-blocking tickets</td>
    <td>within 2 hours</td>
  </tr>
  <tr style="background-color: #a9a9a9; color:black;">
    <td>P2 - Serious</td>
    <td>Update</td>
    <td>every day</td>
  </tr>
  <tr style="background-color: #d3d3d3; color:black;">
    <td>P3 - Medium/Low</td>
    <td>Taking charge on non-critical questions</td>
    <td>within 48 hours</td>
  </tr>
  <tr style="background-color: #a9a9a9; color:black;">
    <td>P3 - Medium/Low</td>
    <td>Resolution</td>
    <td>according to estimate</td>
  </tr>
</table>
