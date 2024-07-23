---
title: Links to organize later
weight: 40
geekdocNav: true
geekdocAnchor: true
---

- [Keep a changelog](https://keepachangelog.com) Don’t let your friends dump git logs into changelogs.


Diagram test:


```plantuml
@startuml
Alice -> Bob : here is my secret
Bob -> Alice : So I see
@enduml
```


![Alt text](https://g.gravizo.com/svg?
@startuml;
actor User;
participant "First Class" as A;
participant "Second Class" as B;
participant "Last Class" as C;
User -> A: DoWork;
activate A;
A -> B: Create Request;
activate B;
B -> C: DoWork;
activate C;
C --> B: WorkDone;
destroy C;
B --> A: Request Created;
deactivate B;
A --> User: Done;
deactivate A;
@enduml
)