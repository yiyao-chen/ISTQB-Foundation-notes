# 2 Testing Throughout the Software Development Lifecycle

## 2.1 Software Development Lifecycle Models
A software development lifecycle model describes the types of activity performed at each stage in a software development project, and how the activities relate to one another logically and chronologically.

**Sequential development models**
Describes the software development process as a linear, sequential flow of activities. This means that any phase in the development process should begin when the previous phase is complete.
Example: Waterfall model

**Iterative and incremental development models**
The software’s features grow incrementally. Iterative development occurs when groups of features are specified, designed, built, and tested together in a series of cycles, often of a fixed duration.
Examples: Rational Unified Process, Scrum, Kansan, Spiral

## 2.2 Test Levels

-   Component testing
    
-   Integration testing
    
-   System testing
    
-   Acceptance testing

### 2.2.1 Component Testing
Focus on components that are separately testable. **Objectives** include:
-  Reducing risk
-  Verifying whether the functional and non-functional behaviors of the component are as designed and specified
    
-   Building confidence in the component’s quality
    
-   Finding defects in the component
    
-   Preventing defects from escaping to higher test levels

**Test basis**
-   Detailed design
    
-   Code
    
-   Data model
    
-  Component specifications

**Test objects**
-   Components, units or modules
    
-   Code and data structures
    
-   Classes
    
-   Database modules
**Typical defects and failures**
-   Incorrect functionality (e.g., not as described in design specifications)
    
-   Data flow problems
    
-   Incorrect code and logic

### 2.2.2 Integration Testing
Focuses on interactions between components or systems. 
**Objectives**
-   Reducing risk
    
-   Verifying whether the functional and non-functional behaviors of the interfaces are as designed and specified
    
-   Building confidence in the quality of the interfaces
    
-   Finding defects (which may be in the interfaces themselves or within the components or systems)
    
-   Preventing defects from escaping to higher test levels

**Two levels of integration Testing**
- Component integration testing
	Performed after component testing. Focuses on the interactions and interfaces between integrated components
- System integration testing
	Focuses on the interactions and interfaces between systems, packages, and microservices. System integration testing can also cover interactions with, and interfaces provided by, external organizations (e.g., web services).

**Test basis**
-   Software and system design
    
-   Sequence diagrams
    
-   Interface and communication protocol specifications
    
-   Use cases
    
-   Architecture at component or system level
    
-   Workflows
    
-   External interface definitions

**Test objects**
-   Subsystems
    
-   Databases
    
-   Infrastructure
    
-   Interfaces
    
-   APIs
    
-   Microservices

**Typical defects and failures**
Examples of typical defects and failures for component integration testing include:
-   Incorrect data, missing data, or incorrect data encoding
    
-   Incorrect sequencing or timing of interface calls
    
-   Interface mismatch
    
-   Failures in communication between components
    
-   Unhandled or improperly handled communication failures between components
    
-   Incorrect assumptions about the meaning, units, or boundaries of the data being passed between components
    

Examples of typical defects and failures for system integration testing include:

-   Inconsistent message structures between systems
    
-   Incorrect data, missing data, or incorrect data encoding
    
-   Interface mismatch
    
-   Failures in communication between systems
    
-   Unhandled or improperly handled communication failures between systems
-  Incorrect assumptions about the meaning, units, or boundaries of the data being passed between systems
    
-   Failure to comply with mandatory security regulations

### 2.2.3 System Testing
Focuses on the behavior and capabilities of a whole system or product, often considering the end-to-end tasks the system can perform and the non-functional behaviors it exhibits while performing those tasks.
**Objectives**
-   Reducing risk
    
-   Verifying whether the functional and non-functional behaviors of the system are as designed and specified

-   Validating that the system is complete and will work as expected
    
-   Building confidence in the quality of the system as a whole
    
-   Finding defects
    
-   Preventing defects from escaping to higher test levels or production

**Test basis**
-   System and software requirement specifications (functional and non-functional)
    
-   Risk analysis reports
    
-   Use cases
    
-   Epics and user stories
    
-   Models of system behavior
    
-   State diagrams
    
-   System and user manuals

**Test objects**
-   Applications
    
-   Hardware/software systems
    
-   Operating systems
    
-   System under test (SUT)
    
-   System configuration and configuration data
    
**Typical defects and failures**
-   Incorrect calculations
    
-   Incorrect or unexpected system functional or non-functional behavior
    
-   Incorrect control and/or data flows within the system
    
-   Failure to properly and completely carry out end-to-end functional tasks
    
-   Failure of the system to work properly in the system environment(s)
    
-   Failure of the system to work as described in system and user manuals

### 2.2.4 Acceptance Testing
Focuses on the behavior and capabilities of a whole system or product.
**Objectives**
-   Establishing confidence in the quality of the system as a whole
-   Validating that the system is complete and will work as expected
-   Verifying that functional and non-functional behaviors of the system are as specified

Common forms of acceptance testing:
- User acceptance testing
Focused on validating the fitness for use of the system by intended users in a real or simulated operational environment. The main objective is building confidence that the users can use the system to meet their needs, fulfill requirements, and perform business processes with minimum difficulty, cost, and risk.
- Operational acceptance testing
	- Testing of backup and restore
	- Installing, uninstalling and upgrading
	- Disaster recovery
	- User management
	- Maintenance tasks
	- Data load and migration tasks
	- Checks for security vulnerabilities
	- Performance testing
- Contractual and regulatory acceptance testing
	- Conractual acceptance testing is performed against a contract’s acceptance criteria for producing custom-developed software. 
	- Regulatory acceptance testing is performed against any regulations that must be adhered to, such as government, legal, or safety regulations.
- Alpha and beta testing
Alpha testing is performed at the developing organization’s site, not by the development team, but by potential or existing customers, and/or operators or an independent test team. Beta testing is performed by potential or existing customers, and/or operators at their own locations. Beta testing may come after alpha testing, or may occur without any preceding alpha testing having occurred.

**Test basis**
-   Business processes
-   User or business requirements
-   Regulations, legal contracts and standards
-   Use cases and/or user stories
-   System requirements
-   System or user documentation
-   Installation procedures
-   Risk analysis reports

**Typical test objects**
-   System under test
-   System configuration and configuration data
-   Business processes for a fully integrated system
-   Recovery systems and hot sites (for business continuity and disaster recovery testing)
-   Operational and maintenance processes
-   Forms
-   Reports
-   Existing and converted production data  

**Typical defects and failures **
-   System workflows do not meet business or user requirements
-   Business rules are not implemented correctly
-   System does not satisfy contractual or regulatory requirements
-   Non-functional failures such as security vulnerabilities, inadequate performance efficiency under high loads, or improper operation on a supported platform


## Test Types
### 2.3.1 Functional Testing
Consider the behaviour of the software. The thoroughness can be measured through functional coverage. 

### 2.3.2 Non-functional Testing
Evaluates characteristics of systems and software such as usability, performance efficiency or security. Testing of "how well" the system behaves. The thoroughness can be measured through non-functional coverage. 

### 2.3.3 White-box Testing
White-box testing derives tests based on the system’s internal structure or implementation. Internal structure may include code, architecture, work flows, and/or data flows within the system. The thoroughness can be measured through structural coverage. 

### 2.3.4 Change-ralated Testing
When changes are made to a system, either to correct a defect or because of new or changing functionality, testing should be done to confirm that the changes have corrected the defect or implemented the functionality correctly, and have not caused any unforeseen adverse consequences.
- Confirmation testing
Reexecute failed test cases after a defect is fixed
- Regression testing 
Detect unintended regressions (side effects)

## 2.4 Maintenance Testing
When any changes are made as part of maintenance, maintenance testing should be performed, both to evaluate the success with which the changes were made and to check for possible side-effects (e.g., regressions) in parts of the system that remain unchanged (which is usually most of the system). Maintenance can involve planned releases and unplanned releases (hot fixes).

### 2.4.1 Triggers for Maintenance
- Modification, such as enhancements, corrective and emergency changes, changes of the operational environment (such as planned operating system or database upgrades), upgrades of COTS software, and patches for defects and vulnerabilities
- Migration, such as from one platform to another, which can require operational tests of the new environment as well as of the changed software, or tests of data conversion when data from another application will be migrated into the system being maintained.

### 2.4.2 Impact Analysis for Maintenance
Impact analysis evaluates the changes that were made for a maintenance release to identify the intended consequences as well as expected and possible side effects of a change, and to identify the areas in the system that will be affected by the change. Impact analysis can also help to identify the impact of a change on existing tests. The side effects and affected areas in the system need to be tested for regressions, possibly after updating any existing tests affected by the change.

Impact analysis can be difficult if:
-   Specifications (e.g., business requirements, user stories, architecture) are out of date or missing
-   Test cases are not documented or are out of date
-   Bi-directional traceability between tests and the test basis has not been maintained
-   Tool support is weak or non-existent
-   The people involved do not have domain and/or system knowledge
-   Insufficient attention has been paid to the software's maintainability during development
