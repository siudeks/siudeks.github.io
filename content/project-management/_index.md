---
title: Project management
weight: 20
geekdocNav: true
geekdocAnchor: true
---

## Story points

*Story points* klasyfikujemy jako *skalę porządkową* (ordinal scale) gdzie możliwe są tylko operacje: *przypisanie* i *porządkowanie*. Nnie klasyfikujemy jako skalę przedziałową (interval scale) gdzie byłoby możliwe wykonywanie *operacji matematycznych* jak *dodawanie czy odejmowanie punktów*. Więcej o skalach pomiatrowych [tutaj](https://cyrkiel.info/statystyka/skale-pomiarowe)

## Powerful Questions

- Do wymagań: Jak będzie to prezentowane przy odbiorze
- Do cache'owania: jak i kiedy cache ma być inwalidowany?
- Do tworzenia zasobów: jak i kiedy mają być zwalniane?

## User Story flow

Available states for tickets are: 

- Not Started: (Owner: Product Team, meaning: poposal / draft)
- Active Product: (Owner: Product Team, meaning: preparing content and acceptance criteria)
- Ready for estimation: TBD
- Estimated by Dev: TBD
- Sprint candidates: TBD
- Ready for QA: TBD
- Ready for Product Acceptance,: TBD
- Ready for Deployment: TBD
- Ready for UAT: TBD
- Closed: TBD

## Sprint flow

- Each sprint starts on Tuesday and it takes two weeks to finish
- Each ticket, where developers are starting some work, has to be assigned to the person who started the work. Later on the same person will be responsible to describe testing scenarios about the ticket for S & T purposes
- On the first day we have planning (about 4 hours)
  - On the planing we are reviewing already prioritized list of issued in state 'Sprint candidates' and we are moving them to the current sprint as far as we have capacity to make some commitment about developing them with the end of the spring. To be clear: developing is not the same as 'deploying them' with the end of the sprint, because QA needs some more time with promoting them from 'Ready for QA' to to 'Ready for product testing' state.
  - Each issue, when started, has automatically its owner from dev team. Such person is responsible for monitoring if all tasks (related to the issue) are done, the owner tests locally the change and - if working - changes  status to 'Ready for QA'
- Day before last we have code freeze
  - Code freeze allow to stop dynamic changes in codebase and allow to polish last fixes on SIT environment by QA
  - SIT image can be promoted to higher environments (Staging, Production)
- On the last day of the sprint (it is Monday) we are fixing code and preparing for Show & tell at the evening
  - Show & Tell: Covers list of developed features grouped as major and minor issues (features / bugs). Both teams - dev team and product team - are on the meeting
  - As the first activity at the morning the team prepare list of items to be presented for show & tell:
    - each team member, having assigned a ticket on the spring backlog, describes on a special Team channel what is the ticket, how to present them, and if it is major or minor change
    - the person, who will present S & T later on at the evening, collects all description, groups them to 'Major' and 'Minor' and tests scenarios on an environment (SIT or STG)
- Every Thursday morning we (as dev team) are reviewing list of 'Ready for estimate' items from Product Team backlog and commenting what we what is unclear and should be discussed on PBR session. We are reviewing from top to down (with assumption they are already prioritized)  If the list is longer then out time-box, we areview as much as we can commenting with questions. The meeting is called 'Pre-PBR session'.
- Every Thursday evening dev team and product team are invited to PBR session, where all items are reviewed from top to down according their priority. Each bug / user story (hereafter: US) is reviewed, Product team shortly explain  background, assumptions and - the most important - Acceptance Criteria (hereafter: AC). At that point we are discussing comments form PBR and any other question which need to be clarify so later on we can estimate such bugs / USs.
- Every Friday morning dev team is reviewing already discussed list of 'Ready for estimate' product backlog items (hereafter: PBI) and estimating them. Each estimated item is moved from 'Ready for estimation' to 'Estimated by dev' so that Product Owner later on can review them ind move from ''Estimated by dev' to 'Sprint candidates' and apply desired priority.

## Polityka urlopowa

- Urlopy obejmujące dni kalendarzowe 4+ są zgłaszane na 2+ sprinty do przodu. Czyli, jeżeli dzisiaj trwa sprint n, to urlop może się zaczynać najwcześniej z datą startową sprint n+2
- Branie w pojedynczym sprincie urlopów 2-3 dni kalendarzowe mogą być zgłaszane na następny sprint
- Pojedynczy dzień urlop w sprincie może być zgłaszany na wg potrzeb
- Urlop, które go zatwierdzenie spowodowałoby że nie będzie projektowej obstawy jakiejś części developmentu (front, backend, infra, testing) będzie odrzucony. W Waszym interesie jest więc wnioskować o urlopy wcześniej niż koledzy. Oczywiście jeżeli jesteś jedyną osobą w substreamie front, backend, infra czy testing urlop Twój, pomimo że "zostawisz" swój substream niebsadzony na czas urlopu, nie jest blokerem dla udzielenia urlopu
- Niestosowanie się do powyższych reguł może (ale nie musi) skutkować odrzuceniem urlopu

## Release policy

- No releases on Friday

## Coding standards

- Green IntelliJ rule: make IntelliJ happy by solving its warnings in just edited files
- Do not produce and expect null values in domain. Potential null values from an external world (like database, API layer) should be normalized using propert actions (e.g. null object pattern, optionals, vavr functional types like Either or, at least, as Jetbrains @Nullable annotation)
- Prove the bulletproof of your changes by adding new test(s), updating existing tests
- - Do not left commented out code without an explanation why it is commented. Such code should be removed by other team members.