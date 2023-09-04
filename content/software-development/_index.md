---
title: Various technical notes
weight: 30
geekdocNav: true
geekdocAnchor: true
---

# Notes

My favorite links and notes

## Some working laws and rules

- [Conways Law](http://www.melconway.com/Home/Conways_Law.html)
- [Amdahl's Law](https://en.wikipedia.org/wiki/Amdahl%27s_law)
- [Sunk cost](https://en.wikipedia.org/wiki/Sunk_cost)
- [INVEST](https://blog.ageno.pl/jak-definiowac-wymagania-zadan-w-projektach/)
- [BRIEF](https://cucumber.io/blog/bdd/keep-your-scenarios-brief-%281%29/)
- [Fallacies of distributed computing](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)
- [Law od Demeter](https://en.wikipedia.org/wiki/Law_of_Demeter)
- [MoSCoW classification](https://en.wikipedia.org/wiki/MoSCoW_method)

## Free comprehensive books:

  - [InfoQ minibooks](https://www.infoq.com/minibooks/)
  - [Programming Notes for Professionals books](https://goalkicker.com/)

## Learning paths / courses

- [Developer Roadmaps](https://roadmap.sh/) as learning path


### My recommendations in 2019

- How to group DDD topics [Awesome DDD](https://github.com/heynickc/awesome-ddd)
- How to organize announcements based on GitHub - based on [dotnet](https://github.com/dotnet/announcements)
- Hewitt, Meijer and Szyperski: [The Actor Model (everything you wanted to know...)](https://www.youtube.com/watch?v=7erJ1DV_Tlo)

### My recommendations in 2018

- [Data Consistency in Microservice Using Sagas](https://www.infoq.com/presentations/saga-microservices/) by Chris Richardson (creator of [Eventuate](https://eventuate.io/)) published 2018/I
topics saga pattern, microservices, data consistency  
Well, he shares practical advices how to use sagas with compensation instead to use ACID transactions. It is quite close to my experience, so I would like to recommed it.
- [From Zero to Hero with Spring WebSocket](https://www.youtube.com/watch?v=nxakp15CACY&feature=youtu.be) by Sergi Almar, recorded at SpringOne2GX 2015
topics java, Spring, WebSockets, SockJS, STOMP
Very practical example how to use (and understand) STOMP over SockJS to two way communication between JS and Java. Have you wondered how to practically use WebSockets? It is for you.

### My recommendations in 2017

- [an Introduction to CQRS & Axon](https://www.infoq.com/presentations/cqrs-axon/?utm_source=presentations_about_axon-framework&utm_medium=link&utm_campaign=axon-framework) by Allard Buijze on Aug 31, 2014  
topics: java, CQRS  
Ineresting introduction why Allard have created Axon framework. I especially like his example with explosing of domain models and spaghetti SQL.
- [Event Sourcing on the JVM](https://www.infoq.com/presentations/event-sourcing-jvm/) by Greg Young.  
topics: java, event sourcing  
Quite good presentation (52 mins), first half contains live-based examples why event sourcing is a natural way of storing changes, and why sql database is not. The second half of the presentation is about jvm implementatsion worth to be considered as event sourcing in your's java application.
- [BDD & DDD](https://www.infoq.com/presentations/bdd-and-ddd/)  
topics: BDD, DDD (what a surprise)  
Solid explanation what is DDD and BDD, without a technical implementations but with examples. Good to share among devs, QAs and BAs.

### Interesting topics  

#### Monads

- [Options and Try monads in Java](https://dzone.com/articles/whats-wrong-java-8-part-iv)
- [Options and Try monads in Scala](https://www.coursera.org/lecture/progfun2/lecture-1-4-monads-98tNE)


### How to contribute
Bug reporting

[Source: linuxconf 2015](https://fr.slideshare.net/jpetazzo/how-to-contribute-to-large-open-source-projects-like-docker-linuxcon-2015)

What makes a bad bug report??

- Emailing the user mailing list
- Emailing the maintainers directly
- Emailing the wrong people (e.g. of a different project)
- "It doesn't work"
- Rage tweet
- No follow-up (when you find the root cause / solution, or realize it was all your fault)

What makes a good bug report?

- Use the bug tracker where there is one
- Look for duplicates
- Look for instructions about filling bugs (should you use tags? run special commands?)
- Three parts:
  - when I do ____
  - I'm expecting ____ to happen
  - But instead, I'm seeing _

Include relevant versions and logs

Note: yes, “relevant” is subjective and therefore hard

Code review
*[Source: thoughtbot](https://github.com/thoughtbot/guides/tree/main/code-review)

A guide for reviewing code and having your code reviewed.

Everyone

- Accept that many programming decisions are opinions. Discuss tradeoffs, which you prefer, and reach a resolution quickly.
- Ask good questions; don't make demands. ("What do you think about naming this :user_id?")
- Good questions avoid judgment and avoid assumptions about the author's perspective.
- Ask for clarification. ("I didn't understand. Can you clarify?")
- Avoid selective ownership of code. ("mine", "not mine", "yours")
- Avoid using terms that could be seen as referring to personal traits. ("dumb", "stupid"). Assume everyone is intelligent and well-meaning.
- Be explicit. Remember people don't always understand your intentions online.
- Be humble. ("I'm not sure - let's look it up.")
- Don't use hyperbole. ("always", "never", "endlessly", "nothing")
- Don't use sarcasm.
- Keep it real. If emoji, animated gifs, or humor aren't you, don't force them. If they are, use them with aplomb.
- Talk synchronously (e.g. chat, screensharing, in person) if there are too many "I didn't understand" or "Alternative solution:" comments. Post a follow-up comment summarizing the discussion.

Having Your Code Reviewed

- Be grateful for the reviewer's suggestions. ("Good call. I'll make that change.")
- A common axiom is "Don't take it personally. The review is of the code, not you." We used to include this, but now prefer to say what we mean: Be aware of [how hard it is to convey emotion online](https://www.fastcompany.com/3036748/why-its-so-hard-to-detect-emotion-in-emails-and-texts) and how easy it is to misinterpret feedback. If a review seems aggressive or angry or otherwise personal, consider if it is intended to be read that way and ask the person for clarification of intent, in person if possible.
- Keeping the previous point in mind: assume the best intention from the reviewer's comments.
- Explain why the code exists. ("It's like that because of these reasons. Would it be more clear if I rename this class/file/method/variable?")
- Extract some changes and refactorings into future tickets/stories.
- Link to the code review from the ticket/story. ("Ready for review: https://github.com/organization/project/pull/1")
- Push commits based on earlier rounds of feedback as isolated commits to the branch. Do not squash until the branch is ready to merge. Reviewers should be able to read individual updates based on their earlier feedback.
- Seek to understand the reviewer's perspective.
- Try to respond to every comment.
- Wait to merge the branch until Continuous Integration (TDDium, TravisCI, etc.) tells you the test suite is green in the branch.
- Merge once you feel confident in the code and its impact on the project.

Reviewing Code

- Understand why the change is necessary (fixes a bug, improves the user experience, refactors the existing code). Then:
- Communicate which ideas you feel strongly about and those you don't.
- Identify ways to simplify the code while still solving the problem.
- If discussions turn too philosophical or academic, move the discussion offline to a regular Friday afternoon technique discussion. In the meantime, let the author make the final decision on alternative implementations.
- Offer alternative implementations, but assume the author already considered them. ("What do you think about using a custom validator here?")
- Seek to understand the author's perspective.
- Sign off on the pull request with a 👍 or "Ready to merge" comment.

## Interesting comments found on the internet

- Remove the ............................. because of limited usage and effort required to maintain it is significant.
- First of all, as already said many times, courtesy is appreciated here. Things like Hi, Thx...
- I want to keep my technology zoo at a minimum.
- Closing the issue as there is no reproduction case provided. Feel free to ask for reopening if it is still actual.
- Please don't comment on closed issue. It's difficult enough to follow development here, but if you use the issue-tracker as kind of "chat-support-system" then things become very difficult.
- Thanks for reaching out and providing feedback. We are working hard on improving the app experience. Can you please elaborate further about the issue?
- You forgot to ask a question (in a problem description on Stack Overflow)
- This is extremely painful. Any issues with (...) can break an entire projects and require extensive manual intervention with advanced, potentially dangerous procedures to remedy.

Interesting facts

- [2017] Kafka performance shines by design: [100k messages per second](https://tanzu.vmware.com/developer/blog/understanding-the-differences-between-rabbitmq-vs-kafka/)
- [2015] It is doable to serve [600k idle concurrent websocket connections using Node.js](https://blog.jayway.com/2015/04/13/600k-concurrent-websocket-connections-on-aws-using-node-js/) on AWS EC2 instance (4CPU 16GB memory)
- [2014] Akka Actor size is about 400 bytes [Effective Actors](https://www.infoq.com/presentations/akka-scala-actor-patterns/?utm_source=presentations_about_scalaio-2013)
- [2003] Eric Evans published [Domain-Driven Design - Tackling Complexity in the Heart of Software](https://en.wikipedia.org/wiki/Domain-driven_design)
- [1973] [Carl Hewitt](https://en.wikipedia.org/wiki/Carl_Hewitt) published [A universal modular ACTOR formalism for artificial intelligence](https://dl.acm.org/doi/10.5555/1624775.1624804)