# Backup Policy

## Purpose
This document aims to define the methods and responsibilities for the proper management of database backups and archives containing personal data, as well as the management and storage of removable media and data restoration in the event of data loss or integrity issues.

Equipment failures, accidental errors, and deliberate attacks can result in the loss of important data. Therefore, measures need to be activated to ensure the availability and continuity of services by creating backup copies that allow for the recovery of damaged information.

## Backup Criteria
Backups are stored remotely.

Backups are encrypted at rest and in transit.

Backups are only accessible to internal IT members.

Backups are retained for at least 1 year.

Restoration procedures are tested at least every 6 months.

An inventory of backups is kept up to date.

If the backup process causes unavailability of the respective service, it will be conducted during non-working hours.

## Backup and Restoration Procedure
For each service, the internal IT team assesses the need for backups. Services that may be excluded from backups are:
- Services used for testing purposes.
- Non-critical services for the company.
- Services that provide high availability and fault recovery strategies.

For all other services, a customized procedure is defined by the internal IT team based on acceptable risk and data importance.

In detail:

- Backup procedure
- Restoration procedure
- Backup scheduling
- Backup frequency

All backups are stored in a dedicated AWS S3 bucket.

For all services that undergo backups, whether manual or automatic, the following must be specified:

- Backup execution date
- Author
- Storage location

The following document provides the status of backups for each company service.

# Services Management

## Data Restoration Procedures
In the event of data loss or damage to critical services, partial or complete data restoration is possible. The restoration is performed by the Data Controller or by an authorized individual appointed by the Data Controller.

The restoration procedure depends on the specific service and is defined by the internal IT team, as mentioned earlier.

## Training and Information for Personnel
In line with the principle of accountability, this procedure will be widely disseminated through:

Sharing on the company's public space (SharePoint).

Presentation in training courses designed within the company on the subject matter.

## Adoption and Review of the Procedure
This procedure is effective immediately and will be constantly updated in light of organizational, technical, and regulatory changes that occur in the field.