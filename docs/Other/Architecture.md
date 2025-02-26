

# Overview

Architecture in Agile Lab is a practice that must be enforced in all projects and porducts.

# Process


1. At the beginning of each project, the {% role %}Engine/COO{% endrole %} assigns an {% role %}Engine/Architecture & Research/Architect{% endrole %} to it
2. The {% role %}Engine/Architecture & Research/Sales Architect{% endrole %} briefs the Architect about all the information he gathered during pre-sale and the high level proposal that was presented
3. The Architect conducts any additional meeting with the customer in order to better understand the functional, technical, strategic and political context
4. The Architected defines the HLD, ensuring he's following the "Well Architected Checklist" that the circle maintains on sharepoint
5. The Architect defines the system sizing or validates the sizing done during pre-sales
6. The Architect defines, based on project complexity, whether an LLD is needed or not
7. The project team following the HLD will generate the LLD if necessary, this will serve also as a bottom-up validation of the HLD
8. The LLD will be validated by the architect; *then iterates the last 5 steps until validation is successful*
9. The Architect remains supportive for the duration of the project and if difficulties or unforeseen events arise, it provides help on architectural themes
10. When needed, the Architect will guide system performance analyses and track the results, sharing them with the circle

# Accountabilities

1. Define the technological stack, among those defined at the business strategy level. Technology means infrastructure and application frameworks, languages, libraries and external services
2. Produce the HLD and store any documentation produced during this phase
3. Decide if LLD is deemed necessary or not
4. Validate the LLD and store any documentation produced during this phase

# HLD

The HLD will be represented by a power point presentation with editable diagrams. The purpose of this document is to give a logical representation of the architecture (so without expressing technologies, but only concepts) and then to decline this in physical architecture (choosing frameworks, components, languages and services).
HLD also cares about breaking the system into macro-components and giving it a nomenclature.

In the document there will be a first part of context, in which will be described the functional, technical, strategic and political context.

HLD diagrams should be commented extensively in slide notes, motivating choices (because one technology instead of another, doubts and reasoning).

The document must be versioned on each iteration inside the "Architecture" sharepoint and then published also into the project specific Sharepoint.

Depending on the duration of the project and the "architectural" effort that is assigned to the project, the Architect might also keep track of evolving architectural decisions using the Architectural Decision Record framework specifically [MADR format](https://adr.github.io/madr/).

# Conventions

All the documentation will be stored into "The Elevator" sharepoint under "architecture".

Folder location for HLD:    `/Customer/Project`

Documents naming convention:  `Customer_Project_TypeOfDoc_Version_Status`

Version: incremental and start from 1

Status: `Draft` | `Final` 

# Architectural Guidelines

In the "The Elevator" sharepoint under "architecture" is easy to find a document "Guidelines.pptx" with all the recommended frameworks, tools and languages. Also, some architectural BluePrints of the most frequent use cases is present.

