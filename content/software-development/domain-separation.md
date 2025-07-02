---
title: Domain models separation
weight: 30
geekdocNav: true
geekdocAnchor: true
---

## Domain models
 - Application defines and uses well-defined set of well-known *domain models*
 - Domain (business) logic operates on *domain models*
 - *Domain models* aren't used directly in any kind of operations with external systems like (de)serialization to files/databases/JSON types/binary types/messages/configuration etc.
 - Proper mappers between external systems and the domain logic are located in proper separated modules/packages (hereafter: ports) related to such external systems so that the domain is still free from being polluted by external types/dependencies.
 - Domain models should be immutable when possible to prevent unexpected side effects.
 - Validation of domain models should occur at creation time to ensure they always represent valid business entities.