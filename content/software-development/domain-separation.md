---
title: Domain models separation
weight: 30
geekdocNav: true
geekdocAnchor: true
---

## Domain models
 - Application defines and uses a well-defined set of well-known *domain models*
 - Domain (business) logic operates on *domain models*
 - *Domain models* aren't used directly in any kind of operations with external systems like (de)serialization to files/databases/JSON types/binary types/messages/configuration etc. even if it is tempting to reuse them in such ways
 - Mappers between external systems and the domain logic are located in dedicated modules/packages (hereafter: ports) related to such external systems so that the domain remains free from being polluted by external types/dependencies.
 - Domain models should be immutable when possible to prevent unexpected side effects.
 - Validation of domain models should occur at creation time to ensure they always represent valid business entities.