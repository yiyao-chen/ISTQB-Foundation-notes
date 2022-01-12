# 5 Test Management

## 5.1 Test Organization

### 5.1.1 Independent Testing
Degrees of independence in testing include the following (from low level of independence to high level):  
-  No independent testers; the only form of testing available is developers testing their own code  
-  Independent developers or testers within the development teams or the project team; this could  be developers testing their colleagues’ products  
-  Independent test team or group within the organization, reporting to project management or  executive management  
-  Independent testers from the business organization or user community, or with specializations in specific test types such as usability, security, performance, regulatory/compliance, or portability  
-  Independent testers external to the organization, either working on-site (in-house) or off-site (outsourcing)
- 
Potential benefits of test independence include:  
-  Independent testers are likely to recognize different kinds of failures compared to developers  
because of their different backgrounds, technical perspectives, and biases  
-  An independent tester can verify, challenge, or disprove assumptions made by stakeholders during specification and implementation of the system  
-  Independent testers of a vendor can report in an upright and objective manner about the system under test without (political) pressure of the company that hired them  
- 
Potential drawbacks of test independence include:  
-  Isolation from the development team, may lead to a lack of collaboration, delays in providing feedback to the development team, or an adversarial relationship with the development team  
-  Developers may lose a sense of responsibility for quality  
-  Independent testers may be seen as a bottleneck  
-  Independent testers may lack some important information (e.g., about the test object)

### Tasks of a Test Manager and Tester
The test manager is tasked with overall responsibility for the test process and successful leadership of the test activities.

Typical test manager tasks may include:  
-  Develop or review a test policy and test strategy for the organization  
-  Plan the test activities by considering the context, and understanding the test objectives and risks. This may include selecting test approaches, estimating test time, effort and cost, acquiring resources, defining test levels and test cycles, and planning defect management  
-  Write and update the test plan(s)  
-  Coordinate the test plan(s) with project managers, product owners, and others  
-  Share testing perspectives with other project activities, such as integration planning  
-  Initiate the analysis, design, implementation, and execution of tests, monitor test progress and results, and check the status of exit criteria (or definition of done) and facilitate test completion activities  
-  Prepare and deliver test progress reports and test summary reports based on the information gathered  
-  Adapt planning based on test results and progress (sometimes documented in test progress reports, and/or in test summary reports for other testing already completed on the project) and  take any actions necessary for test control  
-  Support setting up the defect management system and adequate configuration management of testware  
-  Introduce suitable metrics for measuring test progress and evaluating the quality of the testing and the product  
-  Support the selection and implementation of tools to support the test process, including  
recommending the budget for tool selection (and possibly purchase and/or support), allocating time and effort for pilot projects, and providing continuing support in the use of the tool(s)  
-  Decide about the implementation of test environment(s)  
-  Promote and advocate the testers, the test team, and the test profession within the organization  
-  Develop the skills and careers of testers (e.g., through training plans, performance evaluations, coaching, etc.)

Typical tester tasks may include:  
-  Review and contribute to test plans  
-  Analyze, review, and assess requirements, user stories and acceptance criteria, specifications, and models for testability (i.e., the test basis)  
-  Identify and document test conditions, and capture traceability between test cases, test  
conditions, and the test basis  
-  Design, set up, and verify test environment(s), often coordinating with system administration and network management  
-  Design and implement test cases and test procedures  
-  Prepare and acquire test data  
-  Create the detailed test execution schedule  
-  Execute tests, evaluate the results, and document deviations from expected results  
-  Use appropriate tools to facilitate the test process  
-  Automate tests as needed (may be supported by a developer or a test automation expert)  
-  Evaluate non-functional characteristics such as performance efficiency, reliability, usability, security, compatibility, and portability  
-  Review tests developed by others  

Depending on the risks related to the product and the project, and the software development lifecycle model selected, different people may take over the role of tester at different test levels. For example, at the component testing level and the component integration testing level, the role of a tester is often done by developers. At the acceptance test level, the role of a tester is often done by business analysts, subject matter experts, and users. At the system test level and the system integration test level, the role of a tester is often done by an independent test team. At the operational acceptance test level, the role of a tester is often done by operations and/or systems administration staff.

## 5.2 Test Planning and Estimation
### 5.2.1 Purpose and Content of a Test Plan
A test plan outlines test activities for development and maintenance projects. Test planning activities may include the following and some of these may be documented in a test plan:  
-  Determining the scope, objectives, and risks of testing  
-  Defining the overall approach of testing  
-  Integrating and coordinating the test activities into the software lifecycle activities  
-  Making decisions about what to test, the people and other resources required to perform the various test activities, and how test activities will be carried out  
-  Scheduling of test analysis, design, implementation, execution, and evaluation activities, either on particular dates (e.g., in sequential development) or in the context of each iteration (e.g., in iterative development)  
-  Selecting metrics for test monitoring and control  
-  Budgeting for the test activities  
-  Determining the level of detail and structure for test documentation (e.g., by providing templates or example documents)

### 5.2.2 Test Strategy and Test Approach
A test strategy provides a generalized description of the test process, usually at the product or organizational level. Common types of test strategies include:  
-  Analytical: This type of test strategy is based on an analysis of some factor (e.g., requirement or risk). Risk-based testing is an example of an analytical approach, where tests are designed and prioritized based on the level of risk.  
-  Model-Based: In this type of test strategy, tests are designed based on some model of some required aspect of the product, such as a function, a business process, an internal structure, or a non-functional characteristic (e.g., reliability). Examples of such models include business process models, state models, and reliability growth models.  
-  Methodical: This type of test strategy relies on making systematic use of some predefined set of tests or test conditions, such as a taxonomy of common or likely types of failures, a list of important quality characteristics, or company-wide look-and-feel standards for mobile apps or web pages.  
- Process-compliant (or standard-compliant): This type of test strategy involves analyzing,  
designing, and implementing tests based on external rules and standards, such as those  
specified by industry-specific standards, by process documentation, by the rigorous identification and use of the test basis, or by any process or standard imposed on or by the organization.  
-  Directed (or consultative):  This type of test strategy is driven primarily by the advice, guidance, or instructions of stakeholders, business domain experts, or technology experts, who may be outside the test team or outside the organization itself.  
-  Regression-averse: This type of test strategy is motivated by a desire to avoid regression of existing capabilities. This test strategy includes reuse of existing testware (especially test cases and test data), extensive automation of regression tests, and standard test suites.  
-  Reactive: In this type of test strategy, testing is reactive to the component or system being tested, and the events occurring during test execution, rather than being pre-planned (as the preceding strategies are). Tests are designed and implemented, and may immediately be executed in response to knowledge gained from prior test results. Exploratory testing is a common technique employed in reactive strategies.

### 5.2.3 Entry Criteria and Exit Criteria (Definition of Ready and Definition of Done)  
Entry criteria define the preconditions for undertaking a given test activity. If entry criteria are not met, it is likely that the activity will prove more difficult, more time-consuming, more costly, and more risky. 

Typical entry criteria include:  
-  Availability of testable requirements, user stories, and/or models (e.g., when following a model-based testing strategy)  
-  Availability of test items that have met the exit criteria for any prior test levels
- Availability of test environment  
-  Availability of necessary test tools  
-  Availability of test data and other necessary resources

Exit criteria define what conditions must be achieved in order to declare a test level or a  
set of tests completed. Entry and exit criteria should be defined for each test level and test type, and will differ based on the test objectives.  

Typical exit criteria include:  
-  Planned tests have been executed  
-  A defined level of coverage (e.g., of requirements, user stories, acceptance criteria, risks, code) has been achieved  
-  The number of unresolved defects is within an agreed limit  
-  The number of estimated remaining defects is sufficiently low  
-  The evaluated levels of reliability, performance efficiency, usability, security, and other relevant  quality characteristics are sufficient

### 5.2.4 Test Execution Schedule
Once the various test cases and test procedures are produced (with some test procedures potentially automated) and assembled into test suites, the test suites can be arranged in a test execution schedule that defines the order in which they are to be run. The test execution schedule should take into account such factors as prioritization, dependencies, confirmation tests, regression tests, and the most efficient  
sequence for executing the tests.  

Ideally, test cases would be ordered to run based on their priority levels, usually by executing the test cases with the highest priority first. However, this practice may not work if the test cases have dependencies or the features being tested have dependencies. If a test case with a higher priority is dependent on a test case with a lower priority, the lower priority test case must be executed first. Similarly, if there are dependencies across test cases, they must be ordered appropriately regardless of their relative priorities. Confirmation and regression tests must be prioritized as well, based on the importance of rapid feedback on changes, but here again dependencies may apply.

### 5.2.5 Factors Influencing the Test Effort  
Test effort estimation involves predicting the amount of test-related work that will be needed in order to meet the objectives of the testing for a particular project, release, or iteration. Factors influencing the test effort may include characteristics of the product, characteristics of the development process, characteristics of the people, and the test results.

**Product characteristics**
-  The risks associated with the product  
-  The quality of the test basis
- The size of the product  
-  The complexity of the product domain  
-  The requirements for quality characteristics (e.g., security, reliability)  
-  The required level of detail for test documentation  
-  Requirements for legal and regulatory compliance  

**Development process characteristics**
-  The stability and maturity of the organization  
-  The development model in use  
-  The test approach  
-  The tools used  
-  The test process  
-  Time pressure  

**People characteristics  **
-  The skills and experience of the people involved, especially with similar projects and products (e.g., domain knowledge)  
-  Team cohesion and leadership  

**Test results  **
-  The number and severity of defects found  
-  The amount of rework required

### 5.2.6 Test Estimation Techniques  
There are a number of estimation techniques used to determine the effort required for adequate testing.  
Two of the most commonly used techniques are:  
-  The metrics-based technique: estimating the test effort based on metrics of former similar projects, or based on typical values  
-  The expert-based technique: estimating the test effort based on the experience of the owners of the testing tasks or by experts

Examples of the metrics-based approach:
- burndown charts (Agile)
- defect removal models (Sequential)

Examples of the expert-based approach:
- planning poker (Agile)
- Wideband Delphi (Sequential)

## 5.3 Test Monitoring and Control
The purpose of test monitoring is to gather information and provide feedback and visibility about test activities. Information to be monitored should be used to assess test progress and to measure whether the test exit criteria, or the testing tasks associated with an Agile project's definition of done, are satisfied, such as meeting the targets for coverage of product risks, requirements, or acceptance criteria.  

Test control describes any guiding or corrective actions taken as a result of information and metrics gathered and (possibly) reported.

Examples of test control actions include:  
-  Re-prioritizing tests when an identified risk occurs (e.g., software delivered late)  
-  Changing the test schedule due to availability or unavailability of a test environment or other resources  
-  Re-evaluating whether a test item meets an entry or exit criterion due to rework

### 5.3.1 Metrics Used in Testing  
Metrics can be collected during and at the end of test activities in order to assess:  
-  Progress against the planned schedule and budget  
-  Current quality of the test object  
-  Adequacy of the test approach  
-  Effectiveness of the test activities with respect to the objectives  

Common test metrics include:  
-  Percentage of planned work done in test case preparation (or percentage of planned test cases implemented)  
-  Percentage of planned work done in test environment preparation  
-  Test case execution (e.g., number of test cases run/not run, test cases passed/failed, and/or test conditions passed/failed)  
-  Defect information (e.g., defect density, defects found and fixed, failure rate, and confirmation test results)  
-  Test coverage of requirements, user stories, acceptance criteria, risks, or code  
-  Task completion, resource allocation and usage, and effort  
-  Cost of testing, including the cost compared to the benefit of finding the next defect or the cost compared to the benefit of running the next test

### 5.3.2 Purposes, Contents, and Audiences for Test Reports  
The purpose of test reporting is to summarize and communicate test activity information, both during and at the end of a test activity (e.g., a test level). The test report prepared during a test activity may be referred to as a test progress report, while a test report prepared at the end of a test activity may be referred to as a test summary report.  
During test monitoring and control, the test manager regularly issues test progress reports for stakeholders. In addition to content common to test progress reports and test summary reports, typical test progress reports may also include:  
-  The status of the test activities and progress against the test plan  
-  Factors impeding progress  
-  Testing planned for the next reporting period  
-  The quality of the test object  

When exit criteria are reached, the test manager issues the test summary report. This report provides a summary of the testing performed, based on the latest test progress report and any other relevant information.  
Typical test summary reports may include:  
-  Summary of testing performed  
-  Information on what occurred during a test period  
-  Deviations from plan, including deviations in schedule, duration, or effort of test activities  
-  Status of testing and product quality with respect to the exit criteria or definition of done  
-  Factors that have blocked or continue to block progress  
-  Metrics of defects, test cases, test coverage, activity progress, and resource consumption. 
-  Residual risks 
-  Reusable test work products produced

## 5.4 Configuration Management
The purpose of configuration management is to establish and maintain the integrity of the component or system, the testware, and their relationships to one another through the project and product lifecycle.  
To properly support testing, configuration management may involve ensuring the following:  
-  All test items are uniquely identified, version controlled, tracked for changes, and related to each  other  
-  All items of testware are uniquely identified, version controlled, tracked for changes, related to each other and related to versions of the test item(s) so that traceability can be maintained throughout the test process  
-  All identified documents and software items are referenced unambiguously in test documentation  

During test planning, configuration management procedures and infrastructure (tools) should be identified and implemented.

## 5.5 Risks and Testing
### 5.5.1 Definition of Risk  
Risk involves the possibility of an event in the future which has negative consequences. The level of risk is determined by the likelihood of the event and the impact (the harm) from that event.  

### 5.5.2 Product and Project Risks  
Product risk involves the possibility that a work product (e.g., a specification, component, system, or test)  may fail to satisfy the legitimate needs of its users and/or stakeholders. When the product risks are associated with specific quality characteristics of a product (e.g., functional suitability, reliability, performance efficiency, usability, security, compatibility, maintainability, and portability), product risks are also called quality risks. Examples of product risks include:  
-  Software might not perform its intended functions according to the specification  
-  Software might not perform its intended functions according to user, customer, and/or stakeholder needs  
-  A system architecture may not adequately support some non-functional requirement(s)  
-  A particular computation may be performed incorrectly in some circumstances  
-  A loop control structure may be coded incorrectly  
-  Response-times may be inadequate for a high-performance transaction processing system  
-  User experience (UX) feedback might not meet product expectations
- 
Project risk involves situations that, should they occur, may have a negative effect on a project's ability to achieve its objectives. Examples of project risks include:  
-  Project issues:  
- - Delays may occur in delivery, task completion, or satisfaction of exit criteria or definition  of done  
- - Inaccurate estimates, reallocation of funds to higher priority projects, or general cost-  
cutting across the organization may result in inadequate funding  
- - Late changes may result in substantial re-work  

-  Organizational issues:  
- - Skills, training, and staff may not be sufficient  
- - Personnel issues may cause conflict and problems  
- - Users, business staff, or subject matter experts may not be available due to conflicting  
business priorities  

-  Political issues:  
- - Testers may not communicate their needs and/or the test results adequately  
- - Developers and/or testers may fail to follow up on information found in testing and  
reviews (e.g., not improving development and testing practices)  
- - There may be an improper attitude toward, or expectations of, testing (e.g., not  
appreciating the value of finding defects during testing)  

-  Technical issues:  
- - Requirements may not be defined well enough  
- - The requirements may not be met, given existing constraints  
- - The test environment may not be ready on time  
- - Data conversion, migration planning, and their tool support may be late  
- - Weaknesses in the development process may impact the consistency or quality of project work products such as design, code, configuration, test data, and test cases  
- - Poor defect management and similar problems may result in accumulated defects and  
other technical debt  

-  Supplier issues:  
- - A third party may fail to deliver a necessary product or service, or go bankrupt  
- - Contractual issues may cause problems to the project

### 5.5.3 Risk-based Testing and Product Quality  
Risk is used to focus the effort required during testing. It is used to decide where and when to start testing and to identify areas that need more attention. Testing is used to reduce the probability of an adverse event occurring, or to reduce the impact of an adverse event. Testing is used as a risk mitigation activity, to provide information about identified risks, as well as providing information on residual (unresolved) risks.  

A risk-based approach to testing provides proactive opportunities to reduce the levels of product risk. It involves product risk analysis, which includes the identification of product risks and the assessment of each risk’s likelihood and impact. The resulting product risk information is used to guide test planning, the specification, preparation and execution of test cases, and test monitoring and control. 

In a risk-based approach, the results of product risk analysis are used to:  
-  Determine the test techniques to be employed  
-  Determine the particular levels and types of testing to be performed (e.g., security testing,  accessibility testing)  
-  Determine the extent of testing to be carried out  
-  Prioritize testing in an attempt to find the critical defects as early as possible  
-  Determine whether any activities in addition to testing could be employed to reduce risk (e.g., providing training to inexperienced designers)  

To ensure that the likelihood of a product failure is minimized, risk management activities provide a disciplined approach to:  
-  Analyze (and re-evaluate on a regular basis) what can go wrong (risks)  
-  Determine which risks are important to deal with  
-  Implement actions to mitigate those risks  
-  Make contingency plans to deal with the risks should they become actual events  

In addition, testing may identify new risks, help to determine what risks should be mitigated, and lower uncertainty about risks.

## 5.6 Defect Management
Defects found during testing should be logged. Any defects identified should be investigated and should be tracked from discovery and classification to their resolution (e.g., correction of the defects and successful confirmation testing of the solution, deferral to a subsequent release, acceptance as a permanent product limitation, etc.).

Typical defect reports have the following objectives:  
-  Provide developers and other parties with information about any adverse event that occurred, to enable them to identify specific effects, to isolate the problem with a minimal reproducing test, and to correct the potential defect(s), as needed or to otherwise resolve the problem  
-  Provide test managers a means of tracking the quality of the work product and the impact on the testing (e.g., if a lot of defects are reported, the testers will have spent a lot of time reporting them instead of running tests, and there will be more confirmation testing needed)  
-  Provide ideas for development and test process improvement  

A defect report filed during dynamic testing typically includes:  
-  An identifier  
-  A title and a short summary of the defect being reported  
-  Date of the defect report, issuing organization, and author  
-  Identification of the test item (configuration item being tested) and environment  
-  The development lifecycle phase(s) in which the defect was observed  
-  A description of the defect to enable reproduction and resolution, including logs, database dumps, screenshots, or recordings (if found during test execution)  
-  Expected and actual results  
-  Scope or degree of impact (severity) of the defect on the interests of stakeholder(s)  
-  Urgency/priority to fix
- State of the defect report (e.g., open, deferred, duplicate, waiting to be fixed, awaiting  
confirmation testing, re-opened, closed)  
-  Conclusions, recommendations and approvals  
-  Global issues, such as other areas that may be affected by a change resulting from the defect  
-  Change history, such as the sequence of actions taken by project team members with respect to the defect to isolate, repair, and confirm it as fixed  
-  References, including the test case that revealed the problem
