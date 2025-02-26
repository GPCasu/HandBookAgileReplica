# Product Development

### Purpose
The product development workflow ensures that all the new features are efficiently conceptualized, developed, and launched by following a structured process, aligning teams, and meeting customer needs and company goals.

### Features Planning

Following the key processes highlighted in the [Product Management](ProductManagement.md) workflow, the outcome of the Product Manager work is a backlog with prioritized items. The backlog is divided into experiences: for every area and/or user persona, the Product Manager defines the features that will be developed along with their priority.

The Delivery Team, composed of developers, designers, and testers, will then take the top items from the backlog and break them down into smaller tasks. These tasks will be estimated and planned. The team processes every item using the steps detailed in the [Product Software Development](ProductSoftwareDevelopment.md) workflow.

In addition to the features, the Delivery Team will also work on technical debt, bugs, and other maintenance tasks. These tasks are also prioritized and planned, but urgent bugs may be addressed immediately. If the bugs are related to customer tickets, the Customer Support team will be involved in the process as described in the [Customer Support](CustomerSupport.md) workflow.

Once all the items are listed and prioritized, the Project Lead updates the issues backlog accordingly, and starts a new development cycle.

### Delivery Cycle

The delivery cycle is based on a SCRUM methodology, with sprints lasting two weeks. The Delivery Team will work on the tasks planned for the sprint, and the Project Lead will monitor the progress and remove any blockers that may arise.

The main ceremonies of the delivery cycle are:
- **Product Grooming**: The Product Manager and the Project Lead review the backlog and prioritize the items for the next sprint. The meeting is performed once before every sprint starts. During this meeting priorities and requirements are discussed, and the team estimates the effort required for each item.
- **Support Planning**: The Project Lead and the Support Team discuss the tasks gathered from customer tickets and prioritize them. The tasks are then added to the backlog and prioritized. Bugs and defects planned for the next sprint, while small fixes and feature requests are planned for future sprints, or sent to the Product Manager for evaluation.
- **Sprint Planning**: Before the beginning of every sprint, the Delivery Team meets to discuss the tasks planned for the sprint. The team breaks down big tasks into smaller items, estimates the effort required, and assigns the tasks to the team members. The team also discusses the sprint goal and the definition of done for all the items.
- **Stand-Up Meeting**: Every day, the Delivery Team meets for a short stand-up meeting. Each team member answers one question: if they have any blockers. The meeting is meant to remove any blockers that may arise. In parallel, every team member updates the status of their tasks on a shared board: every day every team member writes what they worked on the previous day, and what they will work on today. This way, the team can see the progress, and we can easily check the history of the tasks.
- **Retrospective**: At the end of every sprint, the Delivery Team meets to discuss what went well and what could be improved. The team discusses the way of working and the process. The outcome of the meeting is a list of action items that are assigned to different team members. The Project Lead will monitor the progress of the action items and will make sure they are implemented. If needed, the tasks are added to the backlog and prioritized.
- **Internal Review**: Before the end of the sprint, the Delivery Team meets with the Product Manager and the Architects to review the work done. The team discusses the tasks completed, and the tasks that are still in progress. This is a way to check the ongoing work and to make sure that everything is on track. The meeting gives visibility to the work done also to people outside the team, like the Product Manager or the Architects.
- **Demo**: At the end of every sprint, the Delivery Team meets with the the stakeholders (the Product Manager and the Professional Services) to demo the work done. The team shows the features developed, and the stakeholders can provide feedback. The feedback is then used to improve the product and to plan the next sprints.

The cycle repeats with a new sprint every 2 weeks; in particular periods of the year (like Christmas or summer holidays) the cycle may be longer, to allow the team to take some time off, while keeping the development process efficient.

### Continuous Integration and Deployment

The Delivery Team uses a continuous integration and deployment pipeline to automate the build, test, and deployment processes. The code of all the modules is stored in repositories on a version control system, and the pipeline is configured to pull the code from the repository and build it automatically.

Every repository adopts a standard branching model, with a main branch that contains the production-ready code, and feature branches that are used for developing new features.
The pipeline is triggered every time a change is pushed to the repository (for all the branches) and it runs a series of automated tests to ensure the quality of the code. If the tests pass, the code can be merged to the main branch; to do this, the developer creates a merge request, and the code is reviewed by another team member. The code is then merged to the main branch, and the pipeline is triggered again to build the relative artifact. Every pipeline on the main branch creates a new artifactory: a Docker image with a specific tag relative to the latest commit. The pipeline then deploys the image to the development environment, where the code is tested by the Delivery Team.

In some specific repositories, there is the definition of the Helm charts. The Helm charts contain all the images needed to perform a complete deployment of the product. The charts are versioned, and the pipeline is configured to deploy the charts to the Quality Assurance and Demo environment. Those environments are replicas of realistic environments, and are used to test the new features released. The pipelines for these environments are triggered manually, so that the team can decide when to deploy the new features.

Since every environment has its own customizations, the pipelines are configured to use different configurations for every environment. The configurations are stored in a separate repository, and the pipelines are configured to pull the configurations from the repository and deploy them to the target environments.
