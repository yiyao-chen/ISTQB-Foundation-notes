# 1 Fundamentals of Testing
**Key words**

coverage, debugging, defect, error, failure, quality, quality assurance, root cause, test analysis, test basis, test case, test completion, test condition, test control, test data, test design, test execution,  
test implementation, test monitoring, test object, test objective, test oracle, test planning, test procedure, test process, test suite, testing, testware, traceability, validation, verification

## 1.1 What is testing?
Software testing is a process which includes  different activities: test planning, analyzing, designing, and implementing tests, reporting test progress and results, and evaluating the quality of a test object.

Dynamic testing involves the execution of the component or system being tested.

Static testing does not involve the execution of the component or system being tested. (reviewing work products such as requirements, user stories, and source code...)

While testing does involve checking whether the system meets specified requirements, it also involves validation, which is checking whether the system will meet user and other stakeholder needs in its operational environment(s).


### 1.1.1 Typical Objectives of Testing

-   To prevent defects by evaluate work products such as requirements, user stories, design, and code
    
-   To verify whether all specified requirements have been fulfilled
    
-   To check whether the test object is complete and validate if it works as the users and other stakeholders expect
    
-   To build confidence in the level of quality of the test object
    
-   To find defects and failures thus reduce the level of risk of inadequate software quality
    
-   To provide sufficient information to stakeholders to allow them to make informed decisions, especially regarding the level of quality of the test object
    
-   To comply with contractual, legal, or regulatory requirements or standards, and/or to verify the test object’s compliance with such requirements or standards
    
The objectives of testing can vary, depending upon the context of the component or system being tested, the test level, and the software development lifecycle model. These differences may include, for example:

-   During component testing, one objective may be to find as many failures as possible so that the underlying defects are identified and fixed early. Another objective may be to increase code coverage of the component tests.
    
-   During acceptance testing, one objective may be to confirm that the system works as expected and satisfies requirements. Another objective of this testing may be to give information to stakeholders about the risk of releasing the system at a given time.

### 1.1.2 Testing and Debudding
Executing tests can show failures that are caused by defects in the software. Debugging is the development activity that finds, analyzes, and fixes such defects. Subsequent confirmation testing checks whether the fixes resolved the defects.

In Agile development and in some other software development lifecycles, testers may be involved in debugging and component testing.

## 1.2 Why is Testing Necessary?
Rigorous testing of components and systems, and their associated documentation, can help reduce the risk of failures occurring during operation. When defects are detected, and subsequently fixed, this contributes to the quality of the components or systems. In addition, software testing may also be required to meet contractual or legal requirements or industry-specific standards.

### 1.2.1 Testing’s Contributions to Success
-   Having testers involved in requirements reviews or user story refinement could detect defects in these work products. The identification and removal of requirements defects reduces the risk of incorrect or untestable features being developed.
    
-   Having testers work closely with system designers while the system is being designed can increase each party’s understanding of the design and how to test it. This increased understanding can reduce the risk of fundamental design defects and enable tests to be identified at an early stage.
    
-   Having testers work closely with developers while the code is under development can increase each party’s understanding of the code and how to test it. This increased understanding can reduce the risk of defects within the code and the tests.
    
-   Having testers verify and validate the software prior to release can detect failures that might otherwise have been missed, and support the process of removing the defects that caused the failures (i.e., debugging). This increases the likelihood that the software meets stakeholder needs and satisfies requirements.

### 1.2.2 Quality Assurance and Testing
Quality management
- **Quality Assurance**
- - focus on adherence to proper processes 
- - contributes to defect prevention
- - supports proper testing (concerned with proper execution of the entire process)
- Quality Control
- - involves test activities (**Testing**)

## 1.2.3 Errors, Defects, Failures
Error (human mistake) -> Defect  (fault or bug in code or other product) -> Failure (caused due to defects in code or environmental conditions such as radiation and pollution in firmware)

Errors may occur for many reasons:
-   Time pressure
    
-   Human fallibility
    
-   Inexperienced or insufficiently skilled project participants
    
-   Miscommunication between project participants, including miscommunication about requirements and design
    
-   Complexity of the code, design, architecture, the underlying problem to be solved, and/or the technologies used
    
-   Misunderstandings about intra-system and inter-system interfaces, especially when such intra- system and inter-system interactions are large in number
    
-   New, unfamiliar technologies

*Not all unexpected test results are failures. *
False positives - may occur due to errors in the way tests were executed, or due to defects in the test data, the test environment, or other testware, or for other reasons.
False negatives - The inverse situation of false positives 
False negatives - tests that do not detect defects that they should have detected
false positives - reported as defects, but aren’t actually defects.

### 1.2.4 Defects, Root Cause and Effects
The root causes of defects are the earliest actions or conditions that contributed to creating the defects. Root cause analysis can lead to process improvements that prevent a significant number of future defects from being introduced.

E.g.
- Defect: improper calculation of interest in code
- Failure: incorrect interest payments
- Effect: customer conplaints
- Root cause: lack of knowledge og the product owner

## 1.3 Seven Testing Principles
1. Testing shows the presence of defects, not their absence

Testing can show that defects are present, but cannot prove that there are no defects. Testing reduces the probability of undiscovered defects remaining in the software but, even if no defects are found, testing is not a proof of correctness.

2. Exhaustive testing is impossible

Testing everything (all combinations of inputs and preconditions) is not feasible except for trivial cases. Rather than attempting to test exhaustively, risk analysis, test techniques, and priorities should be used to focus test efforts.

3. Early testing saves time and money

To find defects early, both static and dynamic test activities should be started as early as possible in the software development lifecycle. Early testing is sometimes referred to as shift left. Testing early in the software development lifecycle helps reduce or eliminate costly changes (see section 3.1).

4. Defects cluster together

A small number of modules usually contains most of the defects discovered during pre-release testing, or is responsible for most of the operational failures. Predicted defect clusters, and the actual observed defect clusters in test or operation, are an important input into a risk analysis used to focus the test effort (as mentioned in principle 2).

5. Beware of the pesticide paradox

If the same tests are repeated over and over again, eventually these tests no longer find any new defects. To detect new defects, existing tests and test data may need changing, and new tests may need to be written. (Tests are no longer effective at finding defects, just as pesticides are no longer effective at killing insects after a while.) In some cases, such as automated regression testing, the pesticide paradox has a beneficial outcome, which is the relatively low number of regression defects.

6. Testing is context dependent

Testing is done differently in different contexts. For example, safety-critical industrial control software is tested differently from an e-commerce mobile app. As another example, testing in an Agile project is done differently than testing in a sequential software development lifecycle project (see section 2.1).

7. Absence-of-errors is a fallacy

Some organizations expect that testers can run all possible tests and find all possible defects, but principles 2 and 1, respectively, tell us that this is impossible. Further, it is a fallacy (i.e., a mistaken belief) to expect that just finding and fixing a large number of defects will ensure the success of a system. For example, thoroughly testing all specified requirements and fixing all defects found could still produce a system that is difficult to use, that does not fulfill the users’ needs and expectations, or that is inferior compared to other competing systems.

## 1.4 Test process
### 1.4.1 Test Process in Context
Contextual factors that influence the test process include, but are not limited to:
-   Software development lifecycle model and project methodologies being used
-   Test levels and test types being considered
- Product and project risks
- Business domain
- Operational constraints:
- - Budgets and resources
- - Timescales
- - Complexity
- - Contractual and regulatory requirements
- - ...
- Organisational policies and practices
- Required internal and external standards

### 1.4.2 Test Activities and Tasks
A test process consists of the following main groups of activities:
-   Test planning
-   Test monitoring and control
-   Test analysis
-   Test design
-   Test implementation
-   Test execution
-   Test completion

*These activities are often implemented iteratively*

**Test planning**

Involves activities that define the objectives of testing and the approach for meeting test objectives within constraints imposed by the context (e.g., specifying suitable test techniques and tasks, and formulating a test schedule for meeting a deadline). Test plans may be revisited based on feedback from monitoring and control activities. 

**Test monitoring and control**

Test monitoring involves the on-going comparison of actual progress against planned progress using any test monitoring metrics defined in the test plan. Test control involves taking actions necessary to meet the objectives of the test plan.

Test monitoring and control are supported by the evaluation of exit criteria, which are referred to as the definition of done in some software development lifecycle models (see ISTQB-CTFL-AT). For example, the evaluation of exit criteria for test execution as part of a given test level may include:

-   Checking test results and logs against specified coverage criteria
    
-   Assessing the level of component or system quality based on test results and logs
    
-   Determining if more tests are needed (e.g., if tests originally intended to achieve a certain level of product risk coverage failed to do so, requiring additional tests to be written and executed)

**Test analysis**

The test basis is analyzed to identify testable features and define associated test conditions. In other words, test analysis determines **“what to test”** in terms of measurable coverage criteria.

Test analysis includes the following major activities:
    
- Analyzing the test basis appropriate to the test level being considered, for example:
- - Requirement specifications, such as business requirements, functional requirements, system requirements, user stories, epics, use cases, or similar work products that specify desired functional and non-functional component or system behavior

- - Design and implementation information, such as system or software architecture diagrams or documents, design specifications, call flow graphs, modelling diagrams (e.g., UML or entity-relationship diagrams), interface specifications, or similar work products that specify component or system structure

- - The implementation of the component or system itself, including code, database metadata and queries, and interfaces

- - Risk analysis reports, which may consider functional, non-functional, and structural aspects of the component or system

- Evaluating the test basis and test items to identify defects of various types, such as: 
- - Ambiguities
- - Omissions  
- - Inconsistencies  
- - Inaccuracies  
- - Contradictions  
- - Superfluous statements
- - Identifying features and sets of features to be tested
    
- - Defining and prioritizing test conditions for each feature based on analysis of the test basis, and considering functional, non-functional, and structural characteristics, other business and technical factors, and levels of risks
    
- - Capturing bi-directional traceability between each element of the test basis and the associated test conditions

The application of black-box, white-box, and experience-based test techniques can be useful in the process of test analysis to reduce the likelihood of omitting important test conditions and to define more precise and accurate test conditions.

The identification of defects during test analysis is an important potential benefit, especially where no other review process is being used and/or the test process is closely connected with the review process. Such test analysis activities not only verify whether the requirements are consistent, properly expressed, and complete, but also validate whether the requirements properly capture customer, user, and other stakeholder needs.

**Test design**

During test design, the test conditions are elaborated into high-level test cases, sets of high-level test cases, and other testware. Test design answers the question **“how to test?”**

Test design includes the following major activities:
-   Designing and prioritizing test cases and sets of test cases
-   Identifying necessary test data to support test conditions and test cases
-   Designing the test environment and identifying any required infrastructure and tools
-   Capturing bi-directional traceability between the test basis, test conditions, and test cases

**Test implementation**

The testware necessary for test execution is created and/or completed, including sequencing the test cases into test procedures. Test implementation answers the question **“do we now have everything in place to run the tests?”**

Test implementation includes the following major activities:

-   Developing and prioritizing test procedures, and, potentially, creating automated test scripts
    
-   Creating test suites from the test procedures and (if any) automated test scripts
    
-   Arranging the test suites within a test execution schedule in a way that results in efficient test execution (see section 5.2.4)
    
-   Building the test environment (including, potentially, test harnesses, service virtualization, simulators, and other infrastructure items) and verifying that everything needed has been set up correctly
    
-   Preparing test data and ensuring it is properly loaded in the test environment
    
-   Verifying and updating bi-directional traceability between the test basis, test conditions, test cases, test procedures, and test suites

*Test design and test implementation tasks are often combined*
*In exploratory testing and other types of experience-based testing, test design and implementation may occur, and may be documented, as part of test execution*

**Test execution**

Test suites are run in accordance with the test execution schedule. Test execution includes the following major activities:
    
-   Recording the IDs and versions of the test item(s) or test object, test tool(s), and testware
    
-   Executing tests either manually or by using test execution tools
    
-   Comparing actual results with expected results
    
-   Analyzing anomalies to establish their likely causes (e.g., failures may occur due to defects in the code, but false positives also may occur 
    
-   Reporting defects based on the failures observed
    
-   Logging the outcome of test execution (e.g., pass, fail, blocked)
    
-   Repeating test activities either as a result of action taken for an anomaly, or as part of the planned testing (e.g., execution of a corrected test, confirmation testing, and/or regression testing)
    
-   Verifying and updating bi-directional traceability between the test basis, test conditions, test cases, test procedures, and test results.


**Test completion**

Collect data from completed test activities to consolidate experience, testware, and any other relevant information. Test completion activities occur at project milestones such as when a software system is released, a test project is completed (or cancelled), an Agile project iteration is finished, a test level is completed, or a maintenance release has been completed.

Test completion includes the following major activities:
-   Checking whether all defect reports are closed, entering change requests or product backlog items for any defects that remain unresolved at the end of test execution
    
-   Creating a test summary report to be communicated to stakeholders
    
-   Finalizing and archiving the test environment, the test data, the test infrastructure, and other testware for later reuse
    
-   Handing over the testware to the maintenance teams, other project teams, and/or other stakeholders who could benefit from its use
    
-   Analyzing lessons learned from the completed test activities to determine changes needed for future iterations, releases, and projects
    
-   Using the information gathered to improve test process maturity


### 1.4.3 Test Work Products
Test work products are created as part of the test process.

**Test planning work products**

Include one or more test plans. The test plan includes information about the test basis, to which the other test work products will be related via traceability information, as well as exit criteria which will be used during test monitoring and control. 

**Test monitoring and control work products**

Include various types of test reports, including test progress reports produced on an ongoing and/or a regular basis, and test summary reports produced at various completion milestones. All test reports should provide audience-relevant details about the test progress as of the date of the report, including summarizing the test execution results once those become available.


**Test analysis work products**

Include defined and prioritized test conditions, each of which is ideally bi- directionally traceable to the specific element(s) of the test basis it covers. For exploratory testing, test analysis may involve the creation of test charters. Test analysis may also result in the discovery and reporting of defects in the test basis.

**Test design work products**

Test design results in test cases and sets of test cases to exercise the test conditions defined in test analysis. It is often a good practice to design high-level test cases, without concrete values for input data and expected results. Such high-level test cases are reusable across multiple test cycles with different concrete data, while still adequately documenting the scope of the test case. Ideally, each test case is bi- directionally traceable to the test condition(s) it covers.

Test design also results in:
-   the design and/or identification of the necessary test data
-   the design of the test environment
-   the identification of infrastructure and tools

**Test implementation work products**

-   Test procedures and the sequencing of those test procedures
-   Test suites
-   A test execution schedule

**Test execution work products**

-   Documentation of the status of individual test cases or test procedures (e.g., ready to run, pass, fail, blocked, deliberately skipped, etc.)
    
-   Defect reports
    
-   Documentation about which test item(s), test object(s), test tools, and testware were involved in the testing
    
**Test completion work products**
    
Test summary reports, action items for improvement of subsequent projects or iterations, change requests or product backlog items, and finalized testware.


