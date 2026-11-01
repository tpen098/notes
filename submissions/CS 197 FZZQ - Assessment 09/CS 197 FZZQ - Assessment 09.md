---
aliases: []
tags: []
date created: Thursday, October 22nd 2026, 9:57:29 pm
date modified: Sunday, November 1st 2026, 3:32:22 pm
---

# CS 197 FZZQ - Module 09 Assessment

Submitted by Stephen Singer on November 1, 2026

## Software Development Lifecycle

> [!Question] Question 01
> What is the difference between effort, duration, and cost?

These three are fundamental metrics used in project estimation and planning.

- **Effort** is the total amount of labor required to complete a task, typically measured in the amount of time needed by a singular person to accomplish it. It represents the complexity and volume of the work, meaning it remains constant regardless of how many people are assigned to it.
- **Duration** is the actual calendar time required to finish the task. This can often be reduced by assigning more people to the work (excluding communication and coordination overhead).
- **Cost** is the total financial price required to accomplish the task. This includes direct costs, such as tools and equipment, as well as labor costs, which are calculated through the effort and rate of the developers involved.

## Technical Project Manager

> [!Question] Question 02
> Should project managers for software engineering projects have the knowledge and skills in programming to lead those projects effectively? Why or why not?

> [!TLDR] TLDR
> Project managers do not need knowledge and skills in programming to lead effectively.

The primary responsibility of a project manager is to organize the team, manage the schedule, and ensure that high-level requirements are translated into an actionable plan for the implementing team. From the developer's side, they are primarily seen for the estimation, scheduling, and coordination of the project. However, the biggest part of their work is simply facilitating communication and removing roadblocks. They are the essential link between the developers and the stakeholders.

While strong programming knowledge can aid in this linking process, it is not strictly necessary. If developers can be trusted to accurately assess technical feasibility, a technical project manager's input simply becomes another opinion for the team to consider. This input often carries less weight, as it merely serves as a starting point for planning, but the final implementation decisions still come from the development team.

Furthermore, a project manager with only basic programming knowledge is unlikely to provide the level of complex input required by senior developers. In reverse, it is unrealistic to expect a project manager to be more technically adept than the developers themselves. The only exception is if they are expected to act as both the project manager and a lead developer, which is simply too much for one person.

However, a project manager may require significant technical expertise if the project or its target audience is highly technical. For example, to truly understand the scheduling risks of a developer-focused tool, the project manager must be able to empathize with a developer's workflow. Similarly, if the project is a machine learning model optimizer, the project manager needs a working knowledge of machine learning concepts to effectively coordinate the team's milestones. On the other hand, a brokerage-focused application is highly technical in its domain logic, yet it doesn't necessarily require the project manager to have a background in programming.

Ultimately, project managers should focus on organization, risk management, and communication. If they are adept at translating complex stakeholder goals into clear, specific timelines and specifications that a developer can understand, they will perform their work well. Deep programming skills are rarely a strict requirement; the necessary level of technical expertise is always dictated by the specific needs of the project and its team.

## Historical Project Data

> [!Question] Question 03
> What are the advantages and disadvantages of using historical project data for project cost estimation?

The primary advantage of using historical project data is that it jump-starts the estimation conversation. When a team is faced with a completely unfamiliar feature, individual estimates can vary wildly due to the high level of uncertainty. This can unnecessarily delay the process. However, if even one developer has relevant experience from a past project, that uncertainty is significantly reduced. This allows the team to streamline the discussion and build their estimates from a familiar, grounded starting point.

However, relying on historical project data for cost estimation introduces risks of bias and false equivalence. While two projects may appear similar on the surface, their specific requirements often differ significantly. Developers can easily fall into the trap of equating features from different projects, assuming they share the same level of complexity.

In reality, complexity is highly dependent on the existing architecture, available modules, and the team's specific knowledge. A feature that was simple to implement in the past might be much more difficult now if a previously used library has been deprecated, if the current architecture lacks native support, or simply because the original developer had specialized expertise. This bias can persist even when features are only conceptually similar, making historical comparisons an unreliable metric for future planning.

Additionally, historical project data is only as valuable as the accuracy and clarity of the records behind it. If past metrics were poorly measured or documented, relying on them can introduce confusion rather than clarity. This can inadvertently make new features seem more difficult than they actually are, adding a counterintuitive layer of uncertainty to the estimation process.

## Project Management Experience

> [!Question] Question 04
> The idea of project estimation and scheduling may be applied even outside software engineering, e.g. when one does his/her thesis. Have you been involved in project estimation "Project Estimation") and scheduling in the past? (Preferably software engineering projects, but may also be other type of projects) Share your experience. What lessons and/or challenges have you encountered?

Yes, I have been involved in project estimation and scheduling before. The most applicable example is a semester-long capstone project that was a prerequisite for our official undergraduate research project.

In this work, our three-person team was tasked with creating an end-to-end electronic system. We received an analog signal, encoded it into a digital signal, processed it using C, performed data analysis via MATLAB, and finally delivered an electronic signal output. The course required us to develop a detailed estimation and schedule for the project. It was really a subject dedicated to teach us how to manage engineering projects.

Since the requirements were explicitly defined for each high-level step, we were able to create a comprehensive end-to-end Waterfall plan rather than relying on an agile workflow like Scrum. We first identified the required features, performed preliminary calculations on the necessary component values, and assessed the level of encapsulation we could achieve. Afterward, we divided the high-level features into subtasks, assigning an expected level of effort and duration to each while accounting for risks like unknowns, scheduling conflicts, and unforeseen additions. Once all tasks were estimated, we scheduled them to minimize risk, provide buffers, and maximize parallel, individual work.

The main lesson we learned was that uncertainties must always be mitigated. Almost all the unknowns we shrugged off during planning came back to bite us later. At one point, we fell behind schedule because a high-level feature required a complete revamp to complement the others.

The second lesson was that effective planning minimizes communication friction. For the parts we planned in detail with clear documentation, we saved valuable time by avoiding unnecessary meetings, which were difficult to coordinate given our conflicting schedules. When we lacked detail, we sometimes had to pause development until we could reach an agreement. Setting up protocols for agreements and general guidelines for specific issues also helped.

Ultimately, the main challenge we encountered was handling uncertainties that required coordinated redesigns. Because we didn't yet have a strong intuition for electronic design, we always opted to adjust the software aspects to make things easier. As it turned out, the hardware design was actually what needed adjusting. Thankfully, we were able to identify this in time to finish the project on schedule and according to the required specifications.
