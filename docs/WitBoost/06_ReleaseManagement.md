# Release Management

### Purpose

Manages the process of deploying new software versions or updates to customers.

### Release Management Process

The release management process involves planning of a new release, documentation generation, publishing of the artifacts, and the upgrade process for the customers. Every release represents a new stable version of the software that includes new features, enhancements, bug fixes, and security updates. In case of critical bugs or security vulnerabilities, hot-fixes or patches are released to address the issues without waiting for the next stable release.

The release management process ensures that the software is delivered to customers in a controlled and efficient manner, with minimal impacts on their operations.

### Planning

The release planning process involves defining the scope of the release, including the features, enhancements, and bug fixes that will be included. The release plan is created based on the product roadmap (updated with customers feedback) and internal priorities. The release plan is updated accordingly to reflect changes in priorities, customer feedback, or new requirements.

### Tools

Witboost uses semantic versioning (major.minor.patch format) to indicate the significance of changes in each release:
- major versions include significant new features or changes that may not be backward compatible; major releases could include breaking changes or significant migration efforts.
- minor versions include new features, enhancements, and bug fixes that are usually backward compatible; some minor migration efforts may be required.
- patch versions include bug fixes and security updates that are backward compatible.

With every new tag in the repositories, the CI/CD pipeline is triggered to build the software, run the tests, and generate the artifacts. The artifacts are then published to the Witboost's artifact repository, where they are available for download by customers. The artifacts are used first to upgrade the internal environments (quality assurance and demo) to validate the new releases.

Witboost uses Helm to bundle together all the images required from the different repositories to deploy the software in a Kubernetes cluster. The Helm charts are versioned and published to the Witboost's Helm repository, where they are available for download. Customers can directly download the Helm charts to deploy the software in their Kubernetes clusters, and they can customize the values.yaml files to configure the software according to their needs.

### Documentation

Every Witboost release is released with a set of documentation that includes release notes, changelogs, migration guides, and user manuals. The documentation is generated as part of the release process and is published on the Witboost's documentation website. The documentation is also available in the software package for offline access.

Every release includes:
- Release Notes: A summary of the changes, enhancements, and bug fixes included in the release.
- Changelogs: Detailed information about the changes made to the software, including the history of issues closed and pull requests merged.
- Migration guides: Step-by-step instructions for upgrading to the new version, including any migration efforts required.
- Version Matrix: A compatibility matrix that shows which versions of the software modules are included in the release and their compatibility with other modules.

With every release, the documentation is updated to reflect the changes made in the software, including the user manual and the administrator guide. The configurations are updated to reflect the new features and enhancements, and the troubleshooting section is updated to include any new issues or resolutions.

### Upgrade Process

Witboost averages a new stable release every 2 months, with hotfix and patch releases in between.

Since patches and new releases are frequent, Witboost uses an automated deployment process to ensure that customers can easily update their software to the latest version. Witboost provides release notes for each version, detailing the changes, enhancements, and bug fixes included in the release.

Customers are not forced to upgrade to the latest version of Witboost, but they are encouraged to do so to take advantage of new features, enhancements, and bug fixes. Usually releases are backward compatible and require small to no migration at all, so customers usually carry out the migration autonomously. Anyway, Witboost provides support for customers who need assistance with the upgrade process, including migration efforts for all the releases. There is no need to upgrade to intermediate releases when installing a new version, as each release includes all the changes from previous versions (e.g. a customer on version 1.1 can upgrade directly to version 1.3 without installing version 1.2).

Usually all customers perform the migration process in a testing environment first, where they perform some tests (functional, penetration, security, etc) to validate that the new release is working before migrating the production environment. The documentation for each release includes a migration guide that provides step-by-step instructions for upgrading to the new version. The global documentation includes a section on releases containing the release notes and bug fixes for each version.
