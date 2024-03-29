- [Ch1.pptx](#ch1pptx)
	- [What is software?](#what-is-software)
	- [What are the attributes of good software?](#what-are-the-attributes-of-good-software)
	- [What is software engineering?](#what-is-software-engineering)
	- [What are the fundamental software engineering activities?](#what-are-the-fundamental-software-engineering-activities)
	- [What is the difference between software engineering and computer science?](#what-is-the-difference-between-software-engineering-and-computer-science)
	- [What is the difference between software engineering and system engineering?](#what-is-the-difference-between-software-engineering-and-system-engineering)
	- [What are the key challenges facing software engineering?](#what-are-the-key-challenges-facing-software-engineering)
	- [What are the costs of software engineering?](#what-are-the-costs-of-software-engineering)
	- [What are the best software engineering techniques and methods?](#what-are-the-best-software-engineering-techniques-and-methods)
	- [What differences has the web made to software engineering?](#what-differences-has-the-web-made-to-software-engineering)
	- [Essential Attributes of Good Software](#essential-attributes-of-good-software)
	- [Software Process Activities](#software-process-activities)
	- [General issues that affect most software](#general-issues-that-affect-most-software)
	- [Aplication Types](#aplication-types)
	- [Software Engineering Fundementals : Check page 22 of Ch1.pptx](#software-engineering-fundementals-check-page-22-of-ch1pptx)
	- [Web Software Engineering](#web-software-engineering)
	- [Key Points So Far #1](#key-points-so-far-1)
	- [Issues of Professional Responsibility](#issues-of-professional-responsibility)
	- [Ethical Principles: Check page 35 of Ch1.pptx](#ethical-principles-check-page-35-of-ch1pptx)
	- [Key Points So Far #2](#key-points-so-far-2)
- [Ch2.pptx](#ch2pptx)
	- [The software Process](#the-software-process)
	- [Plan-driven and Agile Process](#plan-driven-and-agile-process)
	- [Software Process Models](#software-process-models)
		- [The Waterfall Model](#the-waterfall-model)
		- [Incremental Development](#incremental-development)
		- [Reuse-oriented software engineering](#reuse-oriented-software-engineering)
	- [Software Specification](#software-specification)
	- [Design Activities](#design-activities)
	- [Software Validation](#software-validation)
	- [Testing Stages](#testing-stages)
	- [Key Points So far #3](#key-points-so-far-3)
	- [Topics Passed](#topics-passed)
	- [Boehm's Spiral Model](#boehms-spiral-model)
		- [Spiral Model Sectors](#spiral-model-sectors)
		- [Sprial Model Usage](#sprial-model-usage)
	- [The Rational Unified Process](#the-rational-unified-process)
		- [RUP Phases](#rup-phases)
		- [RUP Iteration](#rup-iteration)
		- [Static workflows in the Rational Unified Process](#static-workflows-in-the-rational-unified-process)
		- [RUP Good Practice](#rup-good-practice)
		- [Key Points So Far #4](#key-points-so-far-4)
- [Ch3.pptx](#ch3pptx)
- [Agile Methods](#agile-methods)
	- [Principles of Agile Methods](#principles-of-agile-methods)
	- [Problems with agile methods](#problems-with-agile-methods)
	- [Extreme Programming](#extreme-programming)
		- [Extreme Programming Release Cycle](#extreme-programming-release-cycle)
		- [Extreme Programming practices](#extreme-programming-practices)
		- [Requirements Scenarios](#requirements-scenarios)
		- [Example of Refactoring](#example-of-refactoring)
		- [Key Points So Far #5](#key-points-so-far-5)
		- [XP Testing Difficulties](#xp-testing-difficulties)
		- [Pair Programming](#pair-programming)
	- [Scrum](#scrum)
		- [The Sprint Cycle](#the-sprint-cycle)
		- [Teamwork in Scrum](#teamwork-in-scrum)
		- [Scrum benefits](#scrum-benefits)
	- [Scaling Out and Scaling Up](#scaling-out-and-scaling-up)
		- [Scaling Up to Large Systems](#scaling-up-to-large-systems)
		- [Scaling Out to Large Companies](#scaling-out-to-large-companies)
	- [Key Points So Far #6](#key-points-so-far-6)

<!-- /TOC -->

# Ch1.pptx
## What is software?
Computer programs and associated documentation. Software products may be developed for a particular customer or may be developed for a general market.

## What are the attributes of good software?
Good software should deliver the required functionality and performance to the user and should be maintainable, dependable and usable.

## What is software engineering?
Software engineering is an engineering discipline that is concerned with all aspects of software production.

## What are the fundamental software engineering activities?
Software specification, software development, software validation and software evolution.

## What is the difference between software engineering and computer science?
Computer science focuses on theory and fundamentals; software engineering is concerned with the practicalities of developing and delivering useful software.

## What is the difference between software engineering and system engineering?
System engineering is concerned with all aspects of computer-based systems development including hardware, software and process engineering. Software engineering is part of this more general process.

## What are the key challenges facing software engineering?
Coping with increasing diversity, demands for reduced delivery times and developing trustworthy software.

## What are the costs of software engineering?
Roughly 60% of software costs are development costs, 40% are testing costs. For custom software, evolution costs often exceed development costs.

## What are the best software engineering techniques and methods?
While all software projects have to be professionally managed and developed, different techniques are appropriate for different types of system. For example, games should always be developed using a series of prototypes whereas safety critical control systems require a complete and analyzable specification to be developed. You can’t, therefore, say that one method is better than another.

## What differences has the web made to software engineering?
The web has led to the availability of software services and the possibility of developing highly distributed service-based systems. Web-based systems development has led to important advances in programming languages and software reuse.

## Essential Attributes of Good Software
- **Maintainability** : Software should be written in such a way so that it can evolve to meet the changing needs of customers. This is a critical attribute because software change is an inevitable requirement of a changing business environment.
- **Dependability and security** : Software dependability includes a range of characteristics including reliability, security and safety. Dependable software should not cause physical or economic damage in the event of system failure. Malicious users should not be  able to access or damage the system.
- **Efficiency** : Software should not make wasteful use of system resources such as memory and processor cycles. Efficiency therefore includes responsiveness, processing time, memory utilisation, etc.
- **Acceptability** : Software must be acceptable to the type of users for which it is designed. This means that it must be understandable, usable and compatible with other systems that they use.

## Software Process Activities
- **Software specification**, where customers and engineers define the software that is to be produced and the constraints on its operation.
- **Software development**, where the software is designed and programmed.
- **Software validation**, where the software is checked to ensure that it is what the customer requires.
- **Software evolution**, where the software is modified to reflect changing customer and market requirements.

## General issues that affect most software
 - Heterogenety *different types of computer and mobile devices*
 - Business and social change
 - Security and trust

## Aplication Types
- **Stand-alone applications** : These are application systems that run on a local computer, such as a PC. They include all necessary functionality and do not need to be connected to a network.
- **Interactive transaction-based applications** : Applications that execute on a remote computer and are accessed by users from their own PCs or terminals. These include web applications such as e-commerce applications.
- **Embedded control systems** : These are software control systems that control and manage hardware devices. Numerically, there are probably more embedded systems than any other type of system.
- **Batch processing systems** : These are business systems that are designed to process data in large batches. They process large numbers of individual inputs to create corresponding outputs.
- **Entertainment systems** : These are systems that are primarily for personal use and which are intended to entertain the user.
- **Systems for modeling and simulation** : These are systems that are developed by scientists and engineers to model physical processes or situations, which include many, separate, interacting objects.
- **Data collection systems** : These are systems that collect data from their environment using a set of sensors and send that data to other systems for processing.
- **Systems of systems** : These are systems that are composed of a number of other software systems.

## Software Engineering Fundementals : Check page 22 of Ch1.pptx

## Web Software Engineering
- Software reuse is the dominant approach for constructing web-based systems.
- Web-based systems should be developed and delivered incrementally.
- User interfaces are constrained by the capabilities of web browsers.
- Web-based systems are complex distributed systems but the fundamental principles of software engineering discussed previously are as applicable to them as they are to any other types of system.
- The fundamental ideas of software engineering, discussed in the previous section, apply to web-based software in the same way that they apply to other types of software system.

## Key Points So Far #1
- Software engineering is an engineering discipline that is concerned with all aspects of software production.
- Essential software product attributes are maintainability, dependability and security, efficiency and acceptability.
- The high-level activities of specification, development, validation and evolution are part of all software processes.
- The fundamental notions of software engineering are universally applicable to all types of system development.  
- There are many different types of system and each requires appropriate software engineering tools and techniques for their development.
- The fundamental ideas of software engineering are applicable to all types of software system.

## Issues of Professional Responsibility
- **Confidentiality (Gizlilik)** : Engineers should normally respect the confidentiality of their employers or clients irrespective of whether or not a formal confidentiality agreement has been signed.
- **Competence (Kabiliyet)** : Engineers should not misrepresent their level of competence. They should not knowingly accept work which is outwith their competence.
- **Intellectual property rights (Fikri hak mülkiyeti)** : Engineers should be aware of local laws governing the use of intellectual property such as patents, copyright, etc. They should be careful to ensure that the intellectual property of employers and clients is protected.
- **Computer misuse (Kötüye kullanım)** : Software engineers should not use their technical skills to misuse other people’s computers. Computer misuse ranges from relatively trivial (game playing on an employer’s machine, say) to extremely serious (dissemination of viruses).

## Ethical Principles: Check page 35 of Ch1.pptx

## Key Points So Far #2
- Software engineers have responsibilities to the engineering profession and society. They should not simply be concerned with technical issues.
- Professional societies publish codes of conduct which set out the standards of behaviour expected of their members.

# Ch2.pptx
## The software Process
- There are many of them but all involve:
    + **Specification** : Defining what the system should do.
    + **Design and implementation** : Defining the organization of the system and implementing the system.
    + **Validation** : Checking that it does what the customer wants.
    + **Evolution** : Changing the system in response to changing customer needs.
- When we describe and discuss processes, we usually talk about the activities in these processes such as **specifying a data model**, **designing a user interface**, etc. and the ordering of these activities. Process descriptions may also include:
- **Products**, which are the outcomes of a process activity.
- **Roles**, which reflect the responsibilities of the people involved in the process.
- **Pre- and post-conditions**, which are statements that are true before and after a process activity has been enacted or a product produced.   

## Plan-driven and Agile Process
- **Plan-driven processes** are processes where all of the process activities are planned in advance and progress is measured against this plan.
- In **agile processes**, planning is incremental and it is easier to change the process to reflect changing customer requirements.

## Software Process Models
- **The waterfall model** : Plan-driven model. Separate and distinct phases of specification and development.
- **Incremental development** : Specification, development and validation are interleaved. May be plan-driven or agile.
- **Reuse-oriented software engineering** : The system is assembled from existing components. May be plan-driven or agile.

### The Waterfall Model
- Phases in waterfall:
    + Requirements analysis and definition
    + System and software design
    + Implementation and unit testing
    + Integration and system testing
    + Operation and maintenance
- The **main drawback** of the waterfall model is the **difficulty of accommodating change after the process is underway**. In principle, **a phase has to be complete before moving onto the next phase**.
- Inflexible partitioning of the project into distinct stages makes it difficult to respond to changing customer requirements. Only appropriate when the req. are well-understood. Few business systems have stable req.
- The waterfall model is mostly used for large systems engineering projects where a system is developed at several sites.

### Incremental Development
- The cost of accommodating changing customer requirements is reduced.
- It is easier to get customer feedback on the development work that has been done.
- More rapid delivery and deployment of useful software to the customer is possible.
- The process is not visible.
- System structure tends to degrade(gerilemek) as new increments are added.  

### Reuse-oriented software engineering
- Based on systematic reuse where systems are integrated from existing components or COTS (Commercial-off-the-shelf) systems.
- Process stages
    + Component analysis;
    + Requirements modification;
    + System design with reuse;
    + Development and integration.
- Reuse is now the standard approach for building many types of business system

## Software Specification
- Req. engineering process
    + Feasibility study
    + Requirements elicitation and analysis
    + Requirements specification
    + Requirements validation

## Design Activities
- **Architectural design**, where you identify the overall structure of the system.
- **Interface design**
- **Component design**
- **Database design**

## Software Validation
- Verification and validation (V & V) is intended to show that a system conforms to its specification and meets the requirements of the system customer.
- Involves checking and review processes and system testing.
- System testing involves executing the system with test cases that are derived from the specification of the real data to be processed by the system.

## Testing Stages
- **Development or component testing** : Individual components are tested independently. Components may be functions or objects or coherent groupings of these entities.
- **System testing** : Testing of the system as a whole. Testing of emergent properties is particularly important.
- **Acceptance testing** Testing with customer data to check that the system meets the customer’s needs.

## Key Points So far #3
- Software processes are the activities involved in producing a software system. Software process models are abstract representations of these processes.
- General process models describe the organization of software processes. Examples of these general models include the ‘waterfall’ model,  incremental development, and reuse-oriented development.
- Requirements engineering is the process of developing a software specification.
- Design and implementation processes are concerned with transforming a requirements specification into an executable software system.
- Software validation is the process of checking that the system conforms to its specification and that it meets the real needs of the users of the system.
- Software evolution takes place when you change existing software systems to meet new requirements. The software must evolve to remain useful.

## Topics Passed
- Coping with change
- Reducing the cost of rework
- Software Prototyping
- Incremental development and delivery

## Boehm's Spiral Model
- Process is represented as a spiral rather than as a sequence of activities with backtracking.
- Each loop in the spiral represents a phase in the process.
- No fixed phases such as specification or design - loops in the spiral are chosen depending on what is required.
- Risks are explicitly assessed and resolved throughout the process.

### Spiral Model Sectors
- **Objective setting** : Specific objectives for the phase are identified.
- **Risk assessment and reduction** : Risks are assessed and activities put in place to reduce the key risks.
- **Development and validation** : A development model for the system is chosen  which can be any of the generic models.
- **Planning** : The project is reviewed and the next phase of the spiral is planned.

### Sprial Model Usage
- Spiral model has been very influential in helping people think about iteration in software processes and introducing the risk-driven approach to development.
- In practice, however, the model is rarely used as published for practical software development.

## The Rational Unified Process
- A modern generic process derived from the work on the UML and associated process.
- Brings together aspects of the 3 generic process models discussed previously.
- Normally described from 3 perspectives
    + A dynamic perspective that shows phases over time;
    + A static perspective that shows process activities;
    + A practive perspective that suggests good practice.

### RUP Phases
- **Inception** : Establish the business case for the system.
- **Elaboration** : Develop an understanding of the problem domain and the system architecture.
- **Construction** : System design, programming and testing.
- **Transition** : Deploy the system in its operating environment.

### RUP Iteration
- **In-phase iteration** : Each phase is iterative with results developed incrementally.
- **Cross-phase iteration** : As shown by the loop in the RUP model, the whole set of phases may be enacted incrementally.

### Static workflows in the Rational Unified Process
- Business modelling
- Requirements
- Analysis and design
- Implementation
- Testing
- Deployment
- Configuration and change management
- Project management
- Environment

### RUP Good Practice
- **Develop software iteratively** : Plan increments based on customer priorities and deliver highest priority increments first.
- **Manage requirements** : Explicitly document customer requirements and keep track of changes to these requirements.
- **Use component-based architectures** : Organize the system architecture as a set of reusable components.
- **Visually model software** : Use graphical UML models to present static and dynamic views of the software.
- **Verify software quality** : Ensure that the software meet’s organizational quality standards.
- **Control changes to software** : Manage software changes using a change management system and configuration management tools.

### Key Points So Far #4
- Processes should include activities to cope with change. This may involve a prototyping phase that helps avoid poor decisions on requirements and design.
- Processes may be structured for iterative development and delivery so that changes may be made without disrupting the system as a whole.
- The Rational Unified Process is a modern generic process model that is organized into phases (inception, elaboration, construction and transition) but separates activities (requirements, analysis and design, etc.) from these phases.

# Ch3.pptx
# Agile Methods
- Focus on the code rather than the design
- Are based on an iterative approach to software development
- Are intended to deliver working software quickly and evolve this quickly to meet changing requirements.
- The **aim** of agile methods is to reduce overheads in the software process (e.g. by limiting documentation) and to be able to respond quickly to changing requirements without excessive rework.
- Product development where a software company is developing a small or medium-sized product for sale.

## Principles of Agile Methods
- Customer involvement
- Inremental delivery
- People not process
- Embrace change
- Maintain simplicity

## Problems with agile methods
- It can be difficult to keep the interest of customers who are involved in the process.
- Team members may be unsuited to the intense involvement that characterises agile methods.
- Prioritising changes can be difficult where there are multiple stakeholders.
- Maintaining simplicity requires extra work.
- Contracts may be a problem as with other approaches to iterative development.

## Extreme Programming
- Perhaps the best-known and most widely used agile method.
- Extreme Programming (XP) takes an ‘extreme’ approach to iterative development.
    + New versions may be built several times per day;
    + Increments are delivered to customers every 2 weeks;
    + All tests must be run for every build and the build is only accepted if tests run successfully.
- Incremental development is supported through small, frequent system releases.
- Customer involvement means full-time customer engagement with the team.
- People not process through pair programming, collective ownership and a process that avoids long working hours.
- Change supported through regular system releases.
- Maintaining simplicity through constant refactoring of code.

### Extreme Programming Release Cycle
- Select user stories for this release
- Break down stories to tasks
- Plan release
- Develop/integrate/test software
- Release software
- Evaluate system and go to step 1

### Extreme Programming practices
- Incremental planning
- Small releases
- Simple design
- Test-first development
    + Writing tests before code clarifies the requirements to be implemented.
    + Tests are written as programs rather than data so that they can be executed automatically. The test includes a check that it has executed correctly. Use test frameworks such as Junit.
    + All previous and new tests are run automatically when new functionality is added, thus checking that the new functionality has not introduced errors.
- Refactoring : Programming team look for possible software improvements and make these improvements even where there is no immediate need for them.
- Pair programming
- Collective ownership
- Continuous integration
- Sustainable pace (~sürdürülebilir hız)
- On-site customer : A representative of the end-user of the system (the customer) should be available full time for the use of the XP team. In an extreme programming process, the customer is a member of the development team and is responsible for bringing system requirements to the team for implementation.

### Requirements Scenarios
- In XP, a customer or user is part of the XP team and is responsible for making decisions on requirements.
- User requirements are expressed as scenarios or user stories.
- These are written on cards and the development team break them down into implementation tasks. These tasks are the basis of schedule and cost estimates.
- The customer chooses the stories for inclusion in the next release based on their priorities and the schedule estimates.

>XP proposes constant code improvement (refactoring) to make changes easier when they have to be implemented.

### Example of Refactoring
- Re-organization of a class hierarchy to remove duplicate code.
- Tidying up and renaming attributes and methods to make them easier to understand.
- The replacement of inline code with calls to methods that have been included in a program library.

### Key Points So Far #5
- Agile methods are incremental development methods that focus on rapid development, frequent releases of the software, reducing process overheads and producing high-quality code. They involve the customer directly in the development process.
- The decision on whether to use an agile or a plan-driven approach to development should depend on the type of software being developed, the capabilities of the development team and the culture of the company developing the system.
- Extreme programming is a well-known agile method that integrates a range of good programming practices such as frequent releases of the software, continuous software improvement and customer participation in the development team.

### XP Testing Difficulties
- Programmers prefer programming to testing and sometimes they take short cuts when writing tests. For example, they may write incomplete tests that do not check for all possible exceptions that may occur.
- Some tests can be very difficult to write incrementally. For example, in a complex user interface, it is often difficult to write unit tests for the code that implements the ‘display logic’ and workflow between screens.
- It difficult to judge the completeness of a set of tests. Although you may have a lot of system tests, your test set may not provide complete coverage.  

### Pair Programming
-In XP, programmers work in pairs, sitting together to develop code.
- This helps develop common ownership of code and spreads knowledge across the team.
- It serves as an informal review process as each line of code is looked at by more than 1 person.
- It encourages refactoring as the whole team can benefit from this.
- Measurements suggest that development productivity with pair programming is similar to that of two people working independently.
- Pairs are created dynamically so that all team members work with each other during the development process.

## Scrum
- The Scrum approach is a general agile method but its focus is on managing iterative development rather than specific agile practices.
- There are three phases in Scrum.
    + The initial phase is an outline planning phase where you establish the general objectives for the project and design the software architecture.
    + This is followed by a series of sprint cycles, where each cycle develops an increment of the system.
    + The project closure phase wraps up the project, completes required documentation such as system help frames and user manuals and assesses the lessons learned from the project.

### The Sprint Cycle
- Sprints are fixed length, normally 2–4 weeks. They correspond to the development of a release of the system in XP.
- The starting point for planning is the product backlog, which is the list of work to be done on the project.
- The selection phase involves all of the project team who work with the customer to select the features and functionality to be developed during the sprint.
- Once these are agreed, the team organize themselves to develop the software. - During this stage the team is isolated from the customer and the organization, with all communications channelled through the so-called ‘Scrum master’.
- The role of the Scrum master is to protect the development team from external distractions.
- At the end of the sprint, the work done is reviewed and presented to stakeholders. The next sprint cycle then begins.

### Teamwork in Scrum
- The ‘Scrum master’ is a facilitator who arranges daily meetings, tracks the backlog of work to be done, records decisions, measures progress against the backlog and communicates with customers and management outside of the team.
- The whole team attends short daily meetings where all team members share information, describe their progress since the last meeting, problems that have arisen and what is planned for the following day. This means that everyone on the team knows what is going on and, if problems arise, can re-plan short-term work to cope with them.

### Scrum benefits
- The product is broken down into a set of manageable and understandable chunks.
- Unstable requirements do not hold up progress.
- The whole team have visibility of everything and consequently team communication is improved.
- Customers see on-time delivery of increments and gain feedback on how the product works.
- Trust between customers and developers is established and a positive culture is created in which everyone expects the project to succeed.

>Scaling up agile methods involves changing basic properties to cope with larger, longer projects where there are multiple development teams, perhaps working in different locations.

## Scaling Out and Scaling Up
- **Scaling up** is concerned with using agile methods for developing large software systems that cannot be developed by a small team.
- **Scaling out** is concerned with how agile methods can be introduced across a large organization with many years of software development experience.
- When scaling agile methods it is essential to maintain agile fundamentals
    + Flexible planning, frequent system releases, continuous integration, test-driven development and good team communications.

### Scaling Up to Large Systems
- For large systems development, it is not possible to focus only on the code of the system. You need to do more up-front design and system documentation
- Cross-team communication mechanisms have to be designed and used. This should involve regular phone and video conferences between team members and frequent, short electronic meetings where teams update each other on progress.
- Continuous integration, where the whole system is built every time any developer checks in a change, is practically impossible. However, it is essential to maintain frequent system builds and regular releases of the system.

### Scaling Out to Large Companies
- Project managers who do not have experience of agile methods may be reluctant to accept the risk of a new approach.
- Large organizations often have quality procedures and standards that all projects are expected to follow and, because of their bureaucratic nature, these are likely to be incompatible with agile methods.
- Agile methods seem to work best when team members have a relatively high skill level. However, within large organizations, there are likely to be a wide range of skills and abilities.
- There may be cultural resistance to agile methods, especially in those organizations that have a long history of using conventional systems engineering processes.

## Key Points So Far #6
- Project managers who do not have experience of agile methods may be reluctant to accept the risk of a new approach.
- Large organizations often have quality procedures and standards that all projects are expected to follow and, because of their bureaucratic nature, these are likely to be incompatible with agile methods.
- Agile methods seem to work best when team members have a relatively high skill level. However, within large organizations, there are likely to be a wide range of skills and abilities.
- There may be cultural resistance to agile methods, especially in those organizations that have a long history of using conventional systems engineering processes.
