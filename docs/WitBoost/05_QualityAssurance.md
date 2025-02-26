# Quality Assurance

### Purpose

Ensures the software is free from defects and meets quality standards before release.

### Test Planning and Strategy

The test planning and strategy is defined by different type of tests and testing tools.

For Witboost, the key testing types are:
- **Functional**, which focus on validating that the software's features work according to the specified requirements:
    - **Unit Testing**: Verifying individual components or functions for correct behavior. Unit tests are written by the developers and executed automatically as part of the continuous integration process. The pipelines are executed for every commit and the results are publicly available;
    - **Integration Testing**: Ensuring that different software modules work seamlessly together; integration tests are not always automated, but developers can test the integration of their code with other modules in the development environment. There is no golden rule for this, since it heavily depends on the complexity of the integration, but the development environment is always updated with the latest version of the main branch, so the whole Feature Team can check if the latest features released are working as expected, and not conflicting with one another;
    - **System Testing**: Assessing the complete system's functionality and performance against specified requirements; the Quality Assurance environment is updated periodically with a stable release, and the Quality Assurance team can check the system as a whole to ensure that all the features work as expected and that the system is stable and reliable. In the Quality Assurance environment, we publish also integrations with third-party services, so that the Quality Assurance team can test external integrations as well;
- **Non-functional** which address aspects like performance, security, usability and reliability, ensuring that the application can handle stress, operates securely and delivers a seamless user experience:
    - **Penetration Testing**: Identifying vulnerabilities in the software and assessing its resistance to cyber attacks. In Witboost, we perform periodic penetration tests to identify potential security vulnerabilities and ensure that the software is secure and compliant with industry standards. The tests are conducted by external security experts who simulate real-world attacks to identify potential weaknesses in the software: the results are shared with the Feature Team and the Product Lead, who address the identified issues and implement the necessary security measures;
    - **Performance Testing**: Measuring the software's responsiveness, stability and scalability under various load conditions; performance testing is executed both by the Feature Team and the Quality Assurance team to ensure that the software can handle peak usage and deliver a consistent user experience. Every time a new feature could be impacted by performance issues, the Feature Team writes performance tests, or perform integration tests directly. The Quality Assurance team, on the other hand, performs stress tests on the Quality Assurance environment: this is usually done by simulating a huge number of elements in the system, elements with a lot of data, or users with limited access to the system. The results are shared with the Feature Team and the Product Lead, who address the identified issues and implement the necessary performance optimizations;
    - **Security Testing**: Identifying potential vulnerabilities in the software and assessing its resistance to various security threats. Periodically the Development Team performs vulnerability assessments and security scans to identify potential security vulnerabilities and ensure that the software is secure and compliant with industry standards. This is done using automated tools that scan the images and the codebase for known vulnerabilities and security issues. A complete scan is performed at every stable release, to understand the security impacts for customers.

### Test Case Development

A crucial element is represented by the Definition of Done (DoD), defined during sprints planning in our development workflow. The DoD sets specific criteria that must be met for a feature or user story to be considered complete, including successful execution of all relevant tests (e.g., unit, integration, system, and user acceptance tests) and resolution of identified defects. By incorporating the DoD into test planning, the team can establish a shared understanding of what it means to deliver fully functional, high-quality software.

Creating test cases is a critical part of the software testing process, as it ensures that every aspect of the application's functionality and performance is thoroughly evaluated. All the test cases are discussed by the Quality Assurance team with the Feature Team and the Product Lead to ensure that they cover all the necessary scenarios and edge cases. The test cases are then executed by the Quality Assurance team to verify that the software meets the specified requirements and quality standards.

#### Automated Testing

Developing and maintaining automated tests is the first way to ensure high standards of quality and also to ensure continuous integration and deployment.
Its primary goal is to improve efficiency and accuracy by running repetitive and time-consuming tests, such as regression and performance checks, faster and more consistently than manual methods.

In Witboost, the automated test are maintained by the Quality Assurance team, and they are run as part of the continuous integration process to ensure that new code changes do not introduce defects or regressions. The automated tests are written using testing frameworks (e.g. WebdriverIO) and are executed automatically by the CI/CD pipeline every night. A report is generated after each test run, highlighting any failures or issues that need to be addressed.

#### Manual Testing

Where automation testing is not feasible or effective we perform manual tests.
These tests are essential for scenarios that require human insight, creativity, or judgment such as evaluating user experience, visual elements, and complex interactions that automated scripts cannot fully capture or replicate.

Whenever a feature is released in the Quality Assurance environment, the Quality Assurance team is briefed on the new feature and its expected behavior by the Feature Team. The team then writes all the needed test cases, and performs manual tests to validate the feature against the specified requirements and quality standards. The results of the manual tests are documented on the reporting system and shared with the Feature Team and Product Lead for review and feedback.

Before every major release all the test cases created are executed by the Quality Assurance team to ensure that no regressions have been introduced. In case of any issues, the Quality Assurance opens bug reports that are then addressed by the Feature Team. Every new patch release is tested by the Quality Assurance team to ensure that the bug fixes have been successfully implemented and that the issues have been resolved.

### Bug Tracking and Reporting

There are no constraint on the tools used for bug tracking and reporting, but in WItboost we use Jira since it is already connected with the Customer Support dashboards; in this way, we can easily connect defects found by the Quality Assurance team, with similar problems highlighted by customers. The Quality Assurance team is responsible for tracking and reporting bugs. The bug reports include detailed information about the issue, such as:
- Scenario Summary: the reporter summarizes the scenario and provides a history reference, such as what happened in previous versions;
- Problem Statement: verbose description of the problem, i.e. what happens;
- Expected Behaviour: what should happen if everything worked correctly;
- Steps to Reproduce: all information needed to reproduce the problem, in a way that the Feature Team can easily understand and replicate the issue;
- Proposed Solution: possible solution to the problem, if known;
- Affected Environment: state the environment where the problem occurred;
- Affected Version: indicate the version of the software where the problem occurred;
- Security Level: indicate the security risk of this bug, and how it could affect the users;
- Priority: indicate the priority of the bug, as perceived by the reporter;

It is extremely important to simplify the issue resolution to attach to all the reports all the relevant screenshots and/or logs.

The Feature Team then investigates the bug, identifies the root cause, and implements a fix. Once the fix is implemented, and the patched software is available in the QUality Assurance environment, the Quality Assurance team retests the feature to ensure that the issue has been resolved.
