# Software Development

### Purpose

Our product software development workflow ensures that all the new features will be efficiently conceptualized, developed and launched by following a structured process, aligning teams and meeting both customers and company needs.
Moreover, it is a crucial method to deliver high quality features and establish elevated quality standards.

### Product Software Development Workflow

This workflow encompasses all stages, from the conception and validation of a new idea to its deployment and involves various actors at each phase.

The key phases of the product development workflow are:
1. Feature's Memorandum of Understanding: The Product Manager outlines the concept and requirements while updating the MOU document accordingly.
2. Prototype UI/UX: The Feature Team and the UX Designer create different prototypes, each highlighting different pros and cons. The final prototype is chosen jointly with the Product Manager.
3. High Level Design: The Architect and the Feature Leader outline the system architecture, key components and interactions. The development efforts are divided into epics and estimated.
4. Low Level Design: The Feature Team decomposes the epics into more granular issues capturing technical decisions.
5. Delivery: The Feature Team implements all the core issues, performs code reviews, and conducts technical tests.
6. Quality Assurance: The Quality Assurance Team (with the help of the Product Manager and Product Lead) conducts functional and end-to-end tests.
7. Feature Release: The Feature Team updates configurations, updates the migration instructions, and releases the feature in a demo environment.
8. Product Release: The Product Lead creates the associated documentation, writes release notes (including the changelogs) and informs existing customers and the marketing department.

The detailed breakdown of all the phases is provided below.


#### Feature's Memorandum of Understanding
In this phase, the Product Manager outlines the concept and requirements while updating the Memorandum of Understanding document. This document is a live document, evolving over time according to the strategic goals and market needs, defined by the Product Manager.
Following this, the Product Lead will form a Feature Team and initiate preliminary hypotheses for its development strategy. A Feature Team consists of different member of the team, with all the needed skills to develop the feature. Among the Feature Team a Feature Lead is appointed, who is responsible for the feature development and delivery.

#### Prototype UI/UX
Prototyping is an essential phase that helps visualize concepts, validates design and usability and enhances collaboration among the actors involved such as the Development Team, the UX Designer, the Product Manager, the Feature Team and Professional Services.
It is crucial for early issue identification, aligning expectations and saving time and resources by refining the product before the development begins.
Ultimately, this leads to a more refined design and a smoother development process.

This phase operates independently of Sprints and its key is the fast iteration process.

The UI/UX prototyping processes consist of the following steps:

1. **Brainstorming**: The UX Designer, Product Manager, Product Lead and Feature Lead conduct a brainstorming session focused on the previously identified MOU feature. The output is typically a preliminary sketch (usually created using Power Point or Miro).

2. **Generation of multiple prototypes**: In this step, the Feature Team, Product Lead, and the UX Designer create different prototypes, each highlighting different pros and cons. The resulting deliverable is a presentation or a set of diagrams (usually created using Power Point or draw.io).

3. **Prototype sharing and feedback collection**: The Feature Team and the Product Lead organize a prototype sharing session to gather feedback from UX Designer, Product Manager and Professional Services. After the shared session, the Product Manager, UX designer and Product Lead choose the final prototype that will be turned into interactive design. If there is no unanimous decision, the second and third steps are repeated and continues iteratively until there is a confirmed prototype that can then move on to the next step.

4. **User-interactive design**: The UX Designer translate the prototype sketch into a user-interactive design producing a sharable prototype (usually created using XD or Figma). This prototype is then shared with the Product Lead, Product Manager and Professional Services for feedback.

5. **User Testing**: the UX Designer, in collaboration with testers, conducts user testing and compiles a User Acceptance Report. The user testing could leverage different techniques, such as A/B testing, usability testing, and user interviews.

6. **Final decision**: the UX Designer reviews the XD or Figma prototype based on test results, making adjustments as necessary (the only things that can be left out are external libraries, feasibility checks or smaller details). The final prototype is chosen jointly with the Product Manager and Product Lead.

Indeed, before moving forward, a quality check is conducted by the Product Manager to ensure that the prototype is aligned with our high quality standard, and that it meets the requirements outlined in the MOU document.
If the prototype does not meet these standards, the process will restart from the second step of the iterative prototyping process (new prototypes generation), until the quality standards are met.


#### High Level Design
An High-Level Design (HLD) is crucial for providing a clear, overarching blueprint of the feature before diving into the development process.
It guides both the detailed design and implementation, ensuring that the final product meets technical specifications and business requirements. This phase operates independently of sprints and should not usually take more than one week.

Our HLD process consist of the following steps:

1. **HLD Definition**: The Architect and the Feature Leader outlines the system architecture, key components and interactions. The output is the definition of a HLD document (usually on Power Point). This document can have open points and questions that need to be answered before moving to the next phase. Also, there could be a list of PoCs or MVPs to be developed to validate the architecture and the feasibility of the feature.

2. **Sharing session**: A sharing session is established to gather feedback from all participants on the HLD.
The roles involved in this meeting are:
  - Architect
  - Feature Leader
  - Feature Team
  - Product Manager
  - Product Lead
  - Tech Module Lead
The feedback is then incorporated into the HLD document, and the team iterates on the design until all concerns are addressed.

3. **Quality gate**: Before proceeding, the Product Manager conducts a quality check to ensure that the HLD aligns with our high standards. If these standards are not met, the process will revert to the HLD Definition phase for further refinement.

4. **Generation of Epics**: Once the HLD document is completed, the developments are divided into epics and the HLD document updated. Product Lead, Product Manager and Feature Leader are accountable for this actions.

5. **Estimation**: Each epic is estimated by the Product Lead and Feature Lead. Usually, the estimation is done in days, but it can be done in story points as well. The epics items are then prioritized based on the estimation and the expected value for the customer. It can happen that some parts of the epics are de-promoted to the backlog, because they are not valuable enough for the customer or they are too complex to be developed in the expected time frame.

6. **Prioritization and planning**: The Product Lead and Product Manager initiate the prioritization and planning of the new feature, adjusting the Feature Team as needed. The goal is to ensure that the development efforts are focused to deliver the highest value to the customer.

During this phase, the Architects and Feature Lead can take decisions by crating Proof of Concepts, Minimum Viable Products, or other technical artifacts to validate the architecture and the feasibility of the feature. This is a key step to ensure that the feature can be developed in the expected time frame and with the expected quality. Also, this is the step where we can explore new technologies and new approaches to solve the problem, and choose the best ones.

#### Low Level Design
A Low Level Design is a conceptual type milestones, represents a way of decomposing the high level requirements in more granular issues. It is done only for the prioritized epics and, as per the other phase, a fast iteration is key. This step operates independently of sprints and should not take more than one week per design.

A single High Level Design can be decomposed into multiple Low Level Designs, each focusing on a specific aspect of the feature. This process ensures that the development team has a clear understanding of the technical requirements and can proceed with the implementation efficiently. Every epic should have one or more Low Level Designs, depending on the complexity of the feature. Keep in mind that writing a Low Level Design is very time consuming, so it is important to write it only for the most complex aspects of the feature.

Our LLD process consist of the following steps:

1. **LLD Production**: In this phase the Feature Team decomposes, on Jira, the epics into more granular issues capturing technical decisions which do not involve writing code (e.g. in the case of a new feature, the LLD could include the definition of the API, the definition of the database schema, the definition of the UI components, etc.). The output is a LLD document that is shared with the Product Manager, Product Lead, Tech Module Lead and Architect.

2. **Rework UI/UX**: The Feature Team and Product Designer create a more extended design thanks to the LLD definition. This design take in consideration labels, colors, UX and details in general. The output is a new prototype that contains all the details needed for the development. It is not mandatory to have a fully working prototype, but it is important that all the aspects that are not implemented in the prototype are covered with a detailed description and a clear understanding of the expected result.

3. **LLD Approval**: In async mode, the Tech Module Leads, Product Lead and Architects confirm the design of the previous stages. If there are details to be changed, the process is repeated iteratively until the design is approved.

4. **Issues**: The Feature Team create the issues on Jira, linked to the epics. Note that the "Definition Of Done" is mandatory for every issue: it should include all the technical aspects and functional requirements.

To check that the Low Level Design reflects the set quality standards, a quality check is conducted by the Product Lead, Architect and Tech Module Lead before proceeding to the next phase. If the set quality standards are not achieved, it means that some more iterations are needed to reach the expected quality, and the process restarts.

#### Delivery

The Delivery phase consist of the following steps:

1. **Kick-Off**: The Feature Lead conducts a kick-off meeting to explain all the details of the feature to the Feature Team. The output of this phase is the planning of the first sprint and the assignment of the issues to the team members.

2. **Issue Implementation**: The Feature Team, in accordance with the planning carried out and the sprints, proceeds to implement the issues. In this step the output is the Git branch and the Merge Request with its description.

3. **Check Compliance**: The Feature Lead checks for compliance between the definition of done and the content of the branch. The process proceeds only if the issues are delivered with unit tests, configuration updates, and documentation.

4. **Code Review**: In this phase, the Feature Lead and the Tech Module Lead insert comments and review notes on the Merge Request. The Feature Team will adjust the development as necessary. The output of this phase is the approval of the Merge Request.

5. **Merge and Deploy**: The Feature Lead and the Tech Module Lead rebase the branch on the main one and update the development environment. The development environment is always updated with the latest version of the main branch, so the whole development team can check if the latest features released are working as expected.

6. **Tests Definition**: The Feature Team writes the functional tests by first defining all the test cases. When executed, a report will be compiled to keep track of the tests performed and the results obtained for all the defined test cases.

Before proceeding to the next step a quality check is conducted by the Product Lead to perform the following checks:
- functionalities: the feature works as expected
- configurations: customers can easily configure the feature
- documentation: the feature is well documented
- impacts for existing customers: the feature does not break existing functionalities

If the set quality standards are not achieved, new issues are created and the process restarts.

#### Quality Assurance

1. **Deploy**: At the end of every sprint, the Product Lead performs the deployment of the main branch in the Quality Assurance environment. The output of this phase includes the creation of a new RC (Release Candidate) and the update of configurations for deploying it in the Quality Assurance environment.

2. **Testing**: Once the deployment is complete and the Quality Assurance environment is updated, the Quality Assurance Team and the Product Manager conduct functional tests. The output of this phase is a report that includes all the test cases and their results. The test cases created by the Feature Team are executed by the Quality Assurance Team, and new test cases are added in case some aspects are not covered.

3. **Test results**: Based on test results, any identified bugs are opened to be addressed and resolved in the current sprint. This phase is managed by the Quality Assurance and the Feature Team, who handle the prioritization and finalization of the issues.

Upon completion of these activities, the Product Lead and Product Manager perform a quality check. Furthermore, before releasing the feature, the Product Lead compares the estimated timelines with the actual time taken for delivery. If there are changes to the LLD (Low-Level Design) during development, re-validation through the formal process is not required. The key is to ensure that any changes are clearly communicated to all relevant actors involved.

When a feature is completed, and at the end of every sprint where a milestone is reached, the Feature Team will demonstrate the feature to the Product Manager and the Professional Services Team. This is an opportunity to gather feedback and ensure that the feature meets the requirements outlined in the MOU document.

#### Feature Release
The Feature Release consist of the following steps:

1. **Configurations and Installation**: The Feature Team and Product Lead update the configurations for all the environments, the installation steps note, and the sandbox checklist.

2. **Release Note**: The Feature Team write down the migration notes in the installation repository

3. **Release in Demo**: The Product Lead release the feature in the demo environment.

Note that for any new feature that is intrinsic to the core Witboost environment and needs to be integrated into the Playground environments as well, it's important to update the Playground provisioning checklist accordingly. Anyway, the Feature Team should always inform the Infrastructure Team that in the next iterations of the Playground, the newly introduced feature and any related changes must be incorporated into the environments, and all the necessary configurations must be updated.

In this phase, it is necessary to:

- Document in the installation repository all the steps that the customer needs to follow to install the new version.
- Update in the configurations' repository the configuration files for the internal environments.

#### Product Release

The product release is managed by the Product Lead, and it results in a new version of the product that is available to the customers. The Product Lead is responsible for creating the associated documentation, writing release notes (including the changelogs) and informing existing customers and the marketing department. In particular, the Product Lead will:
- create a new stable tag for all the repositories involved in the release;
- create a new stable tag for all the Helm charts;
- generate the changelogs for the release;
- write the release notes with the new features and the bug fixes;
- generate a security report for the release;
- inform the marketing department about the new release;
- inform the customers about the new release.

The Product Lead will also update the documentation repository with the new version of the documentation (which is anyway shipped along with the product in the Helm charts).
