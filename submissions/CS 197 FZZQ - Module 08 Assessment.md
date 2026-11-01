---
aliases: []
tags: []
date created: Thursday, October 22nd 2026, 9:57:29 pm
date modified: Friday, October 23rd 2026, 6:44:14 pm
---

# CS 197 FZZQ - Module 08 Assessment

Submitted by Stephen Sabas Singer on October 23, 2026

## Software Development Lifecycle

> [!Question] Question 01
> Have you engaged in software development projects before? Discuss which phase of the Software Development Life Cycle did you practice the most and which you did not. How could your more overlooked phase/s of SDLC have helped you or your team execute your past projects better?

> [!TLDR] TLDR
> Yes, I've engaged in software development projects across varying levels of team structures. Across both experiences, the development phase has always been my primary focus, while the design phase remains the most consistently overlooked area that could significantly improve project execution if properly invested in.

In my first company, we operated in a small working group where each developer handled an entire project end-to-end. Because we had a mature, streamlined deployment pipeline, deployment was the least invested phase.

Most of our effort centered heavily on the **development phase**, driven by complex technical requirements from end users. The second most time-consuming stage was the **analysis phase**, which required scheduling multiple stakeholder meetings to untangle complex business domains.

Meanwhile, the **planning phase** received the second least investment. Working individually fostered an immediate "build a working prototype first and iterate" mindset. However, overlooking upfront planning created bottlenecks in medium-to-large applications; rushing straight into implementation led to tightly coupled codebases that made subsequent refactoring difficult and painful.

In my current company, we follow a traditional agile team structure divided into cross-functional roles including product owners, business analysts, scrum masters, developers, and testers. Developers engage in the analysis phase during ticket refinement, transition to the design phase once assigned an epic, and then move into development. Testers handle final test approvals, while deployment and maintenance are managed through a rotating system of release coordinators and tech support.

Even in this structured environment, the **design phase** remains the most critical blind spot. Neglecting early architectural coordination has frequently caused developers to write disjointed code in silos. On one notable occasion, a lack of explicitly defined dependencies in the design stage resulted in four different developers independently implementing the exact same feature in four entirely different ways.

## Software Engineer Qualities

> [!Question] Questionion 02
> What should be the qualities of a software engineer? Which qualities have you observed in yourself? Which qualities do you think would you need to improve on in this line of work?

> [!TLDR] TLDR
> A software engineer should be adaptable, articulate, and empathetic.

### Fast-paced Demands

Software requirements can drastically change in ways that make the current working process obsolete. This demands innovations in software techniques. This is why software engineering methods and tools update regularly.

*Software engineers must be prepared to learn new practices to cater to modern systems and users*. If they're not quick to learn, they can cause friction in collaborations, miss crucial deadlines, and become unable to solve newfound challenges in modern systems.

### Communication is Key

The process of creating software is rarely done alone. Even if there is only one developer for a project, there will still be a need to communicate with the user. *Controlling technical abstraction for software design and being mindful of how ideas are expressed ensures clear, organized, and efficient communication to everyone involved in the work.*

There have been far too many examples where miscommunication in the form of missing information, excessive detailing, or disorganized notes have caused weeks worth of bug tickets and misalignment with the users. Vague and unprocessed talks cause these.

An idea to be committed as functional code has to be specific and discussed
Converting ideas to software requires specificity, scope, conciseness, and simplicity to become plannable, testable, documentable, and shippable. These are all qualities of effective communication.

### Working Together

Software is made to solve problems. *Developers need to understand their users' challenges to develop solutions to them.* If the developers are disconnected with their user's perspective, they can create software that may be efficient, easy-to-use, and maintainable, but still ultimately useless.

Additionally, understanding creates opportunities and efficient work. A problem may be a symptom of a deeper bug that a developer can directly address. Maybe a small change in a different workflow can eliminate the user's challenges. UI work especially needs to understand how users perceive the software.

*Empathy for the team is also critical for solving problems faster.* Coding as an activity may be solitary but the problem solving step isn't. Developers can pitch in when their peers are challenged and they need fresh perspectives as opposed to letting each developer silo their knowledge and take longer on some tasks. Experience has shown the overhead of communication is worth the value of solving complex problems quickly. *Coding within software engineering is not a competition either.* Developers can create architectures or systems with the mindset of making other developers' time easier.

### Self-Reflection

I think the quality I resonate with the most is articulation. I opt to over explain in assessments to explicitly show my thought process and practice the Feynman technique. However, I am more articulate in my delivery at work.

In my main work, senior developers have erratic schedules, product owners and business analysts are drowning in meetings, and I'm also busy with features. Any chance to communicate has to be one-shot and not cause confusion. Even for the refinement steps of our ceremonies, there should be no ambiguity and thoughts have to be organized.

In my free time I teach programming and science writing to elementary students up to professionals. Both subjects require outlined, engaging explanations on the spot. This also hones my articulation for my work and reframes my definition of an actual simple approach that a newly onboarded developer would understand.

I also practice **empathy** in my software engineering work. I consistently frame technical decisions around user needs and strive to build maintainable, extensible architectures for my teammates. However, there is still room for me to expand my intuition regarding which engineering practices best empower other developers and to deepen my understanding of broader user behaviors.

The quality I need to further develop is **adaptability**. While I am naturally curious and flexible, I can sometimes fall into a comfort zone when working within stable, familiar systems. Deep domain knowledge often yields quick, reliable solutions using existing tech stacks, which is effective short-term but can inadvertently reduce opportunities to experiment with emerging tools. It also doesn't help that teaching can get repetitive.

This reflection is a key reason I am pursuing this program: to actively push myself out of familiar environments and create a structured demand for learning. I also try to catch up on current tech news and explore new tools I can integrate into my workflow nowadays.

## Readability

> [!Question] Question 03
> In your past programming projects, what practices did you do to ensure that you, your teammates, teacher/evaluator, or anyone who would take interest in your designs and codes are easily understood or modifiable(when necessary)?

> [!TLDR] TLDR
> In all of my programming projects, I mainly work under two software design principles: Separation of Concern (SoC) and Don't Repeat Yourself (DRY).

### Separation of Concern

Decoupling features makes code readable as it minimizes cognitive load. In a decoupled system, developers can focus on specific modules without holding the entire system in their head. It also make code modifiable because its easier to find where to add changes.

I enforce this hierarchically, structuring directories by feature clusters, services into classes, and specific logic into functions using spatial proximity to keep related concepts close together.

Following SOLID principles of OOP, I define explicit contracts via interfaces and protocols to cleanly encapsulate behavior. I strictly follow the Single Responsibility rule as it naturally applies the SoC mentality. This also keeps classes small enough to support inheritance for extension without creating inherited pieces that are unused.

### Don't Repeat Yourself

Another principle I follow is avoiding redundant code. This not only saves space but prevents readers from forming false mental patterns about duplicated logic in disjoint systems. Assuming the same level of complexity and explicitness per piece, less visible code enables readability.

### Documentation

My primary approach to documentation is keeping context close to the implementation through inline doc strings for modules, functions, and classes. While some argue that clean code should be completely self-documenting, experience has taught me that critical edge cases and local intent are best captured directly alongside the code rather than scattered across external wikis.

I still maintain external documentation, but I reserve it for high-level concepts like project architecture, logistics, and design rationale. By striving for readable code, I ensure inline docs focus on essential context rather than redundantly re-explaining self-evident logic.

## User Acceptance

> [!Question] Question 04
> Did you already have any would-be software user for which you designed and created a software for? If yes, what challenges did you encounter in capturing their requirements, and eventually, having them evaluate and adopt/accept your software?

In my previous work, part of my responsibility was handling the development of complex tools for investment bankers when they couldn't build them internally. One notable project was creating an end-to-end dashboard for select accounts they were managing, which included an application frontend, email automation, web scraping, and automated report generation.

The bankers explained their vision as clearly as possible, but I often had to fill in the implementation details. Because non-technical users naturally struggle to articulate technical requirements, I learned to focus strictly on understanding their workflow pain points and translating those into automations they would value. I also had to manage instances where a banker tried to alter the requirements mid-flight based on what they *thought* would be easier for me to code, which actually complicated things further.

Feature acceptance and adoption were smooth precisely because of these iterative check-ins. In earlier projects, I made the mistake of building the final model immediately. I fell into a waterfall trap where early miscommunications compounded into massive rework. Breaking development down into visible, incremental layers kept everyone aligned, paced my work, and shielded non-technical stakeholders from overwhelming technical details.
