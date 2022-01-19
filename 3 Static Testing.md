# 3 Static Testing

## Benefits of static testing
- Enable early detection of defects before dynamic testing is performed
- Preventing defects in design or coding by uncovering inconsistencies, ambiguities, contradictions, omissions, inaccuracies, and redundancies in requirements
-   Increasing development productivity (e.g., due to improved design, more maintainable code)
-   Reducing development/testing cost and time    
-   Reducing total cost of quality over the software’s lifetime, due to fewer failures later in the lifecycle or after delivery into operation
-   Improving communication between team members in the course of participating in reviews

## Differences between Static and Dynamic Testing
One main distinction is that static testing finds defects in work products directly rather than identifying failures caused by defects when the software is run. A defect can reside in a work product for a very long time without causing a failure. The path where the defect lies may be rarely exercised or hard to reach, so it will not be easy to construct and execute a dynamic test that encounters it.

Another distinction is that static testing can be used to improve the consistency and internal quality of work products, while dynamic testing typically focuses on externally visible behaviors.

Compared with dynamic testing, typical defects that are easier and cheaper to find and fix through static testing include:

-   Requirement defects (e.g., inconsistencies, ambiguities, contradictions, omissions, inaccuracies, and redundancies)
-   Design defects (e.g., inefficient algorithms or database structures, high coupling, low cohesion)
-   Coding defects (e.g., variables with undefined values, variables that are declared but never used, unreachable code, duplicate code)
-   Deviations from standards (e.g., lack of adherence to coding standards)
-   Incorrect interface specifications (e.g., different units of measurement used by the calling system than by the called system)
-   Security vulnerabilities (e.g., susceptibility to buffer overflows)
-   Gaps or inaccuracies in test basis traceability or coverage (e.g., missing tests for an acceptance criterion)

Most types of maintainability defects can **only** be found by static testing (e.g., improper modularization, poor reusability of components, code that is difficult to analyze and modify without introducing new defects).

## Review Process

### Work Product Review Process
**Planning**
-   Defining the scope, which includes the purpose of the review, what documents or parts of documents to review, and the quality characteristics to be evaluated
-   Estimating effort and timeframe
-   Identifying review characteristics such as the review type with roles, activities, and checklists
-   Selecting the people to participate in the review and allocating roles
-   Defining the entry and exit criteria for more formal review types (e.g., inspections)
-   Checking that entry criteria are met (for more formal review types)
-   
**Initiate review**
-   Distributing the work product (physically or by electronic means) and other material, such as issue log forms, checklists, and related work products
-   Explaining the scope, objectives, process, roles, and work products to the participants
-   Answering any questions that participants may have about the review 

**Individual review (i.e., individual preparation)**
-   Reviewing all or part of the work product
-   Noting potential defects, recommendations, and questions 

**Issue communication and analysis**
-   Communicating identified potential defects (e.g., in a review meeting)
-   Analyzing potential defects, assigning ownership and status to them
-   Evaluating and documenting quality characteristics
-   Evaluating the review findings against the exit criteria to make a review decision (reject; major changes needed; accept, possibly with minor changes)

**Fixing and reporting**
-   Creating defect reports for those findings that require changes to a work product
-   Fixing defects found (typically done by the author) in the work product reviewed
-   Communicating defects to the appropriate person or team (when found in a work product related to the work product reviewed)
-   Recording updated status of defects (in formal reviews), potentially including the agreement of the comment originator
-   Gathering metrics (for more formal review types)
-   Checking that exit criteria are met (for more formal review types)
-   Accepting the work product when the exit criteria are reached

### Roles and responsibilities in a formal review
Author
-   Creates the work product under review
-   Fixes defects in the work product under review (if necessary) 

Management
-   Is responsible for review planning
-   Decides on the execution of reviews
-   Assigns staff, budget, and time
-   Monitors ongoing cost-effectiveness
-   Executes control decisions in the event of inadequate outcomes

Facilitator (often called moderator)
-   Ensures effective running of review meetings (when held)
-   Mediates, if necessary, between the various points of view
-   Is often the person upon whom the success of the review depends

Review leader
-   Takes overall responsibility for the review
-   Decides who will be involved and organizes when and where it will take place

Reviewers
-   May be subject matter experts, persons working on the project, stakeholders with an interest in the work product, and/or individuals with specific technical or business backgrounds
-   Identify potential defects in the work product under review
-   May represent different perspectives (e.g., tester, developer, user, operator, business analyst, usability expert, etc.)
    
Scribe (or recorder)
   - Collates potential defects found during the individual review activity
        
    - Records new potential defects, open points, and decisions from the review meeting (when held)

### Review Types
**Informal review**
-   Main purpose: detecting potential defects
-   Possible additional purposes: generating new ideas or solutions, quickly solving minor problems
-   May not involve a review meeting
-   May be performed by a colleague of the author (buddy check) or by more people
-   Results may be documented
-   Varies in usefulness depending on the reviewers
-   Use of checklists is optional
-   Very commonly used in Agile development

**Walkthrough**
-   Main purposes: find defects, improve the software product, consider alternative implementations, evaluate conformance to standards and specifications
    
-   Possible additional purposes: exchanging ideas about techniques or style variations, training of participants, achieving consensus
    
-   Individual preparation before the review meeting is optional
    
-   Review meeting is typically led by the author of the work product
    
-   Scribe is mandatory
    
-   Use of checklists is optional
    
-   May take the form of scenarios, dry runs, or simulations
    
-   Potential defect logs and review reports are produced
    
-   May vary in practice from quite informal to very formal

**Technical review**
-   Main purposes: gaining consensus, detecting potential defects
    
-   Possible further purposes: evaluating quality and building confidence in the work product, generating new ideas, motivating and enabling authors to improve future work products, considering alternative implementations
    
-   Reviewers should be technical peers of the author, and technical experts in the same or other disciplines
    
-   Individual preparation before the review meeting is required
    
-   Review meeting is optional, ideally led by a trained facilitator (typically not the author)
    
-   Scribe is mandatory, ideally not the author
    
-   Use of checklists is optional
    
-   Potential defect logs and review reports are produced

**Inspection**
-   Main purposes: detecting potential defects, evaluating quality and building confidence in the work product, preventing future similar defects through author learning and root cause analysis
    
-   Possible further purposes: motivating and enabling authors to improve future work products and the software development process, achieving consensus
    
-   Follows a defined process with formal documented outputs, based on rules and checklists
    
-   Uses clearly defined roles, and may include a dedicated reader (who reads the work product aloud often paraphrase, i.e. describes it in own words, during the review meeting)
    
-   Individual preparation before the review meeting is required
    
-   Reviewers are either peers of the author or experts in other disciplines that are relevant to the work product
-   Specified entry and exit criteria are used
    
-   Scribe is mandatory
    
-   Review meeting is led by a trained facilitator (not the author)
    
-   Author cannot act as the review leader, reader, or scribe
-   Potential defect logs and review reports are produced
-   Metrics are collected and used to improve the entire software development process, including the inspection process

### Review Techniques
**Ad hoc**

Reviewers are provided with little or no guidance on how this task should be performed. Reviewers often read the work product sequentially, identifying and documenting issues as they encounter them. This technique is highly dependent on reviewer skills and may lead to many duplicate issues being reported by different reviewers.

**Checklist-based**

A systematic technique, whereby the reviewers detect issues based on checklists that are distributed at review initiation (e.g., by the facilitator). A review checklist consists of a set of questions based on potential defects, which may be derived from experience. Checklists should be specific to the type of work product under review and should be maintained regularly to cover issue types missed in previous reviews. The main advantage of the checklist-based technique is a systematic coverage of typical defect types. Care should be taken not to simply follow the checklist in individual reviewing, but also to look for defects outside the checklist.

**Scenarios and dry runs**

Reviewers are provided with structured guidelines on how to read through the work product. A scenario-based review supports reviewers in performing “dry runs” on the work product based on expected usage of the work product. These scenarios provide reviewers with better guidelines on how to identify specific defect types than simple checklist entries. As with checklist-based reviews, in order not to miss other defect types (e.g., missing features), reviewers should not be constrained to the documented scenarios.

**Perspective-based**

In perspective-based reading, similar to a role-based review, reviewers take on different stakeholder viewpoints in individual reviewing. Typical stakeholder viewpoints include end user, marketing, designer, tester, or operations. Using different stakeholder viewpoints leads to more depth in individual reviewing with less duplication of issues across reviewers.

In addition, perspective-based reading also requires the reviewers to attempt to use the work product under review to generate the product they would derive from it. 

Empirical studies have shown perspective-based reading to be the most effective general technique for reviewing requirements and technical work products. A key success factor is including and weighing different stakeholder viewpoints appropriately, based on risks.

**Role-based**

A role-based review is a technique in which the reviewers evaluate the work product from the perspective of individual stakeholder roles. Typical roles include specific end user types (experienced, inexperienced, senior, child, etc.), and specific roles in the organization (user administrator, system administrator, performance tester, etc.). The same principles apply as in perspective-based reading because the roles are similar.

### Success Factors for Reviews
Organizational success factors for reviews include:

-   Each review has clear objectives, defined during review planning, and used as measurable exit criteria
    
-   Review types are applied which are suitable to achieve the objectives and are appropriate to the type and level of software work products and participants
    
-   Any review techniques used, such as checklist-based or role-based reviewing, are suitable for effective defect identification in the work product to be reviewed
    
-   Any checklists used address the main risks and are up to date
    
-   Large documents are written and reviewed in small chunks, so that quality control is exercised by providing authors early and frequent feedback on defects

-   Reviews are scheduled with adequate notice
    
-   Management supports the review process (e.g., by incorporating adequate time for review activities in project schedules)
    
-   Reviews are integrated in the company's quality and/or test policies.

People-related success factors for reviews include:

-   The right people are involved to meet the review objectives, for example, people with different skill sets or perspectives, who may use the document as a work input
    
-   Testers are seen as valued reviewers who contribute to the review and learn about the work product, which enables them to prepare more effective tests, and to prepare those tests earlier

-   Reviews are conducted on small chunks, so that reviewers do not lose concentration during individual review and/or the review meeting (when held)

-   Defects found are acknowledged, appreciated, and handled objectively
    
-   The review is conducted in an atmosphere of trust; the outcome will not be used for the evaluation of the participants
    
-   Participants avoid body language and behaviors that might indicate boredom, exasperation, or hostility to other participants

-   A culture of learning and process improvement is promoted
