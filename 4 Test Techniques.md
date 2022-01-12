# 4 Test Techniques
Black-box test
Based on an analysis of the appropriate test basis (e.g., formal requirements documents, specifications, use cases, user stories, or business processes). These techniques are applicable to both functional and non- functional testing. Black-box test techniques concentrate on the inputs and outputs of the test object without reference to its internal structure.

Common characteristics of black-box test techniques include:

- Test conditions, test cases, and test data are derived from a test basis that may include software requirements, specifications, use cases, and user stories

-   Test cases may be used to detect gaps between the requirements and the implementation of the requirements, as well as deviations from the requirements
    
-   Coverage is measured based on the items tested in the test basis and the technique applied to the test basis
- 
White-box test techniques (also called structural or structure-based techniques) are based on an analysis of the architecture, detailed design, internal structure, or the code of the test object. Unlike black-box test techniques, white-box test techniques concentrate on the structure and processing within the test object.

Common characteristics of white-box test techniques include::

-   Test conditions, test cases, and test data are derived from a test basis that may include code, software architecture, detailed design, or any other source of information regarding the structure of the software
    
-   Coverage is measured based on the items tested within a selected structure (e.g., the code or interfaces) and the technique applied to the test basis

Experience-based test techniques leverage the experience of developers, testers and users to design, implement, and execute tests. These techniques are often combined with black-box and white-box test techniques.

Common characteristics of experience-based test techniques include:
 - Test conditions, test cases, and test data are derived from a test basis that may include knowledge and experience of testers, developers, users and other stakeholders

## Black-box Test Techniques
### Equivalence Partitioning
Equivalence partitioning divides data into partitions (also known as equivalence classes) in such a way that all the members of a given partition are expected to be processed in the same way (see Kaner 2013 and Jorgensen 2014). There are equivalence partitions for both valid and invalid values.

-   Valid values are values that should be accepted by the component or system. An equivalence partition containing valid values is called a “valid equivalence partition.”
    
-   Invalid values are values that should be rejected by the component or system. An equivalence partition containing invalid values is called an “invalid equivalence partition.”
    
-   Partitions can be identified for any data element related to the test object, including inputs, outputs, internal values, time-related values (e.g., before or after an event) and for interface parameters (e.g., integrated components being tested during integration testing).
    
-   Any partition may be divided into sub partitions if required.
    
-   Each value must belong to one and only one equivalence partition.
    
-   When invalid equivalence partitions are used in test cases, they should be tested individually, i.e., not combined with other invalid equivalence partitions, to ensure that failures are not masked. Failures can be masked when several failures occur at the same time but only one is visible, causing the other failures to be undetected.
    
To achieve 100% coverage with this technique, test cases must cover all identified partitions (including invalid partitions) by using a minimum of one value from each partition. Coverage is measured as the number of equivalence partitions tested by at least one value, divided by the total number of identified equivalence partitions, normally expressed as a percentage. Equivalence partitioning is applicable at all test levels.

### Boundary Value Analysis
Boundary value analysis (BVA) is an extension of equivalence partitioning, but can only be used when the partition is ordered, consisting of numeric or sequential data. The minimum and maximum values (or first and last values) of a partition are its boundary values.

For example, suppose an input field accepts a single integer value as an input, using a keypad to limit inputs so that non-integer inputs are impossible. The valid range is from 1 to 5, inclusive. So, there are three equivalence partitions: invalid (too low); valid; invalid (too high). For the valid equivalence partition, the boundary values are 1 and 5. For the invalid (too high) partition, the boundary value is 6. For the invalid (too low) partition, there is only one boundary value, 0, because this is a partition with only one member.

In the example above, we identify two boundary values per boundary. The boundary between invalid (too low) and valid gives the test values 0 and 1. The boundary between valid and invalid (too high) gives the test values 5 and 6. 

Some variations of this technique identify three boundary values per boundary: the values before, at, and just over the boundary. In the previous example, using three-point boundary values, the lower boundary test values are 0, 1, and 2, and the upper boundary test values are 4, 5, and 6.

### Decision Table Testing
When creating decision tables, the tester identifies conditions (often inputs) and the resulting actions (often outputs) of the system.

For conditions:

-   Y means the condition is true (may also be shown as T or 1)
    
-   N means the condition is false (may also be shown as F or 0)
    
-   — means the value of the condition doesn’t matter (may also be shown as N/A)

For actions:

-   X means the action should occur (may also be shown as Y or T or 1)
    
-   Blank means the action should not occur (may also be shown as – or N or F or 0)

The common minimum coverage standard for decision table testing is to have at least one test case per decision rule in the table. This typically involves covering all combinations of conditions. Coverage is measured as the number of decision rules tested by at least one test case, divided by the total number of decision rules, normally expressed as a percentage.

### State Transition Testing 
A state transition diagram shows the possible software states, as well as how the software enters, exits, and transitions between states.

A state transition table shows all valid transitions and potentially invalid transitions between states, as well as the events, and resulting actions for valid transitions. State transition diagrams normally show only the valid transitions and exclude the invalid transitions.

Tests can be designed to cover a typical sequence of states, to exercise all states, to exercise every transition, to exercise specific sequences of transitions, or to test invalid transitions.

Coverage is commonly measured as the number of identified states or transitions tested, divided by the total number of identified states or transitions in the test object, normally expressed as a percentage.

### Use Case Testing
Each use case specifies some behavior that a subject can perform in collaboration with one or more actors. Interactions between the actors and the subject may result in changes to the state of the subject. Interactions may be represented graphically by work flows, activity diagrams, or business process models.

A use case can include possible variations of its basic behavior, including exceptional behavior and error handling (system response and recovery from programming, application and communication errors, e.g., resulting in an error message). Tests are designed to exercise the defined behaviors (basic, exceptional or alternative, and error handling). Coverage can be measured by the number of use case behaviors tested divided by the total number of use case behaviors, normally expressed as a percentage.

## White-box Test Techniques
White-box testing is based on the internal structure of the test object. White-box test techniques can be used at all test levels.

### Statement Testing and Coverage

Statement testing exercises the potential executable statements in the code. Coverage is measured as the number of statements executed by the tests divided by the total number of executable statements in the test object, normally expressed as a percentage.

### Decision Testing and Coverage

Decision testing exercises the decisions in the code and tests the code that is executed based on the decision outcomes. To do this, the test cases follow the control flows that occur from a decision point (e.g., for an IF statement, one for the true outcome and one for the false outcome; for a CASE statement, test cases would be required for all the possible outcomes, including the default outcome).

Coverage is measured as the number of decision outcomes executed by the tests divided by the total number of decision outcomes in the test object, normally expressed as a percentage.

### The Value of Statement and Decision Testing

When 100% statement coverage is achieved, it ensures that all executable statements in the code have been tested at least once, but it does not ensure that all decision logic has been tested. Of the two white- box techniques discussed in this syllabus, statement testing may provide less coverage than decision testing.

When 100% decision coverage is achieved, it executes all decision outcomes, which includes testing the true outcome and also the false outcome, even when there is no explicit false statement (e.g., in the case of an IF statement without an else in the code). Statement coverage helps to find defects in code that was not exercised by other tests. Decision coverage helps to find defects in code where other tests have not taken both true and false outcomes.

Achieving 100% decision coverage guarantees 100% statement coverage (but not vice versa).

## Experience-based Test Techniques

When applying experience-based test techniques, the test cases are derived from the tester’s skill and intuition, and their experience with similar applications and technologies. These techniques can be helpful in identifying tests that were not easily identified by other more systematic techniques.

### Error Guessing
Error guessing is a technique used to anticipate the occurrence of errors, defects, and failures, based on the tester’s knowledge, including:

-   How the application has worked in the past
    
-   What kind of errors tend to be made
    
-   Failures that have occurred in other applications
    
    A methodical approach to the error guessing technique is to create a list of possible errors, defects, and failures, and design tests that will expose those failures and the defects that caused them. These error, defect, failure lists can be built based on experience, defect and failure data, or from common knowledge about why software fails.
    
### Exploratory Testing
In exploratory testing, informal (not pre-defined) tests are designed, executed, logged, and evaluated dynamically during test execution. The test results are used to learn more about the component or system, and to create tests for the areas that may need more testing.

Exploratory testing is sometimes conducted using session-based testing to structure the activity. In session-based testing, exploratory testing is conducted within a defined time-box, and the tester uses a test charter containing test objectives to guide the testing. The tester may use test session sheets to document the steps followed and the discoveries made.

Exploratory testing is most useful when there are few or inadequate specifications or significant time pressure on testing. Exploratory testing is also useful to complement other more formal testing techniques.

Exploratory testing is strongly associated with reactive test strategies.

### Checklist-based Testing

In checklist-based testing, testers design, implement, and execute tests to cover test conditions found in a checklist. As part of analysis, testers create a new checklist or expand an existing checklist, but testers may also use an existing checklist without modification.

Checklists can be created to support various test types, including functional and non-functional testing. In the absence of detailed test cases, checklist-based testing can provide guidelines and a degree of consistency.

