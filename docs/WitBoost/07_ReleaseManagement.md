# Security

### Purpose

Ensures the software meets security standards and complies with regulatory requirements.

### Security and Compliance

The main goal of the security process in place is to define a security assessment and threat modeling. To identify potential security threats and vulnerabilities in the software, we adopt the following practices:
* Daily vulnerability scanning of the dependencies and libraries used in the software. This is performed by an automated tool that checks for known vulnerabilities in all the images that we release (CVEs). All the vulnerabilities are categorized based on their severity and are fixed based on the severity level; all the vulnerabilities of level high/critical are resolved as soon as a resolution is released.
* Periodic penetration testing to identify potential security weaknesses in the software. This is performed by a third-party security firm that simulates real-world attacks on the software to identify vulnerabilities that could be exploited by malicious actors. After every penetration test cycle, we receive a detailed report with the identified vulnerabilities and recommendations for remediation, which we address promptly. In case of vulnerabilities found, we release a new version, and we perform another penetration test to ensure that the vulnerabilities have been fixed.
* Regular security code reviews to identify security flaws in the codebase. This is performed manually by the development team during the code review process, where they look for common security issues (such as SQL injection, cross-site scripting, and insecure deserialization, etc). The team also uses a third-party automated tool that performs SAST analysis to identify potential security vulnerabilities in the codebase. The tool provides a report for the development team to review and address any identified issues, and the analysis is performed before every release.
* Regarding compliance with security standards, we as a company also adhere to industry best practices and standards such as ISO 27001 (Security of Information), ISO 27701 (Security of Information according to GDPR), ISO 9001 (Quality System), and ISO 22301 (Business Continuity) to ensure that the software meets the highest security standards.

### Application Security

On a more general scope, Witboost adheres to the following security policies and techniques to ensure comprehensive protection.

#### Authentication and Authorization

Witboost delegates the authentication to a third-party service provider, chosen from a list of supported ones (all main OAuth 2.0 providers are supported, and new ones can be easily integrated); usually customers will use their default providers (like Microsoft Entra ID) which provides a secure and reliable authentication mechanism. The service provider can support different security levels, like multi-factor authentication, and WItboost will integrate with it also to get the organization structure: which users and groups are supported, and how users are assigned to the groups they belong to. This ensures that only authorized users can access the software and that their identities are verified securely.

Authorization is handled through an RBAC (Role-Based Access Control) system, where users and/or groups are assigned roles that determine what actions they can perform in the software. The roles are collections of specific permissions: they are defined based on the user's job function and responsibilities, and they are assigned to users by the administrators. This ensures that users can only access the features and data that are relevant to their role, and that sensitive information is protected from unauthorized access.

The combination of the two mechanisms ensures that the software is secure and that only authorized users can access it, and that it can completely governed from outside Witboost. Even the RBAC mechanism is managed inside Witboost, a customer can define the roles only fro groups, and change the assignment of the users to the groups from the organization provider. In this way, the customer can manage the access to the software without the need to access the software itself. Alternatively, the customer can define the roles and assign them to the users directly from Witboost, and the product will manage the access to the resources.

#### Infrastructure Security

The infrastructure where Witboost is installed, is provided by the customer, and the customer is responsible for the security of the infrastructure. This means that the customer can choose to deploy Witboost on-premises or on a cloud provider, and to provide all the necessary security measures to protect the infrastructure.

Witboost requires a Postgres database, and Kubernetes cluster to run. Usually the Postgres database is provided through a managed service, and the customer can choose to deploy the product on a managed Kubernetes service (like GKE, EKS, or AKS) or on a self-managed Kubernetes cluster. In both cases, the customer is responsible for the security of the cluster.

The customer can implement different security measures to protect the infrastructure, and to make the data reliable (like backups, disaster recovery, and high availability).

Usually, customers choose to deploy Witboost in one or more Kubernetes clusters, and to use a managed Postgres database to store the data. The Kubernetes clusters are not reachable from the internet, and all the communication with the software is done through a reverse proxy that is managed by the customer. If any of the pods need to contact external services, the customer can configure the firewall rules to allow only the necessary traffic.

One important example of external interaction could be between the "Provisioning Coordinator" module, and the Tech Adapters, which are external services that are used to provision the resources in the third-party systems. Since the Tech Adapters are developed and maintained by the customer, but their execution can create/destroy resources in the third-party systems, the customer can deploy them outside of the Kubernetes cluster, and needs to be sure that they are invoked only by the Provisioning Coordinator, which handles the authorization. To ensure that the Tech Adapters are invoked only by the Provisioning Coordinator, Witboost allows you to setup an mTLS (mutual TLS) communication between the two services. This is performed by generating a certificate for the Provisioning Coordinator, and configuring the Tech Adapters to accept only requests that are signed by the certificate. This ensures that only the Provisioning Coordinator can invoke the Tech Adapters, and that the communication is secure.

#### Monitoring and Logging

As already introduced, the deployment of Witboost is managed by the customer, who can decide to deploy it on-premises or on a cloud provider. In both cases, the customer is responsible for the security of the infrastructure. The customer can then access different functionalities to monitor the software and the infrastructure.

Witboost provides an auditing mechanism, which stores all the actions performed by the users in the system. The audit log contains information about the user who performed the action, the action itself, the timestamp, and the resource involved (along with the URL, module, and type of action). The audit log is stored in the database, and it can be accessed by the administrators to review the actions performed by the users and to investigate any suspicious activity.

Every pod has an API that can be invoked to check its health status. This is the same mechanism used by Helm to check the readiness and liveliness of the microservices. The API returns a status code that indicates whether the pod is healthy or not, and it can be used by the administrators to monitor the health of the software and to take action if any issues are detected.

In addition to this, every Witboost's pod (the software is deployed in a microservices architecture) generates logs that can be collected and stored in a centralized logging system. The log level of each pod can be configured by the customer, and the logs can be accessed by the administrators to monitor the health of the software and to troubleshoot any issues that may arise.
