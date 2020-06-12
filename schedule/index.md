<frontmatter>
title: "Schedule"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 1
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "admin/admin-tasks.mbdf" import show_weekly_admin_tasks with context %}

<!--
    {num: "1", day:"Aug 12"},
    {num: "2", day:"Aug 19"},
    {num: "3", day:"Aug 26"},
    {num: "4", day:"Sep 2"},
    {num: "5", day: "Sep 9" },
    {num: "6", day: "Sep 16" },
    {num: "7", day: "Sep 30" },
    {num: "8", day: "Oct 7" },
    {num: "9", day: "Oct 14" },
    {num: "10", day: "Oct 21" },
    {num: "11", day: "Oct 28" },
    {num: "12", day: "Nov 4" },
    {num: "13", day: "Nov 11" }
-->

{% set weeks = [
    {num: "1", day: "from Mon Jan 13"},
    {num: "2", day: "from Wed Jan 15 noon"},
    {num: "3", day: "from Wed Jan 22 noon"},
    {num: "4", day: "from Wed Jan 29 noon"},
    {num: "5", day: "from Wed Feb 5 noon"},
    {num: "6", day: "from Wed Feb 12 noon"},
    {num: "7", day: "from Wed Feb 19 noon"},
    {num: "8", day: "from Wed Mar 4 noon"},
    {num: "9", day: "from Wed Mar 11 noon"},
    {num: "10", day: "from Wed Mar 18 noon"},
    {num: "11", day: "from Wed Mar 25 noon"},
    {num: "12", day: "from Wed Apr 1 noon"},
    {num: "13", day: "from Wed Apr 8 noon"}
] %}

{#
-1: site not ready, lands in the module intro page
0: site ready but semester hasn't started, lands in the module intro page
14: site no longer used, lands in the module intro page
1..13: site is active, lands in the week's schedule page
#}
{% set current_week = "15" %}


{% set all_topics = [
{week: "1"},
{week: "2"},
  {name: "SE Intro"},
    {heading: "SE: Intro"},
      {location: ["softwareEngineering", "introduction", "prosAndCons"]},
  {name: "Java"},
    {heading: "Java: Intro"},
      {location: ["cppToJava", "about"]},
      {location: ["cppToJava", "javaWorld", "what"]},
      {location: ["cppToJava", "javaWorld", "how"]},
      {location: ["cppToJava", "javaWorld", "editions"]},
    {heading: "Java: HelloWorld"},
      {location: ["cppToJava", "gettingStarted", "installation"]},
      {location: ["cppToJava", "gettingStarted", "helloWorld"]},
      {location: ["cppToJava", "gettingStarted", "compiling"]},
      {location: ["cppToJava", "gettingStarted", "running"]},
    {heading: "Java: Data Types"},
      {location: ["cppToJava", "dataTypes", "primitiveTypes"]},
      {location: ["cppToJava", "dataTypes", "variables"]},
      {location: ["cppToJava", "dataTypes", "operators"]},
      {location: ["cppToJava", "dataTypes", "arrays"]},
    {heading: "Java: Control Flow"},
      {location: ["cppToJava", "controlFlow", "branching"]},
      {location: ["cppToJava", "controlFlow", "methods"]},
      {location: ["cppToJava", "controlFlow", "loops"]},
  {name: "Revision Control"},
    {heading: "RCS: Init, Commit"},
      {location: ["revisionControl", "what"]},
      {location: ["revisionControl", "repositories"]},
      {location: ["gitAndGithub", "init"]},
      {location: ["revisionControl", "savingHistory"]},
      {location: ["gitAndGithub", "commit"]},
      {location: ["gitAndGithub", "ignore"]},
    {heading: "RCS: Fork, Clone"},
      {location: ["revisionControl", "remoteRepositories"]},
      {location: ["gitAndGithub", "clone"]},
  {name: "Implementation"},
    {heading: "IDEs: Basic Features"},
      {location: ["ides", "introduction", "what"]},
      {location: ["intellij", "projectSetup"]},
      {location: ["intellij", "codeNavigation"]},
    {heading: "Code Quality: Coding Standards"},
      {location: ["codeQuality", "introduction", "basic"]},
      {location: ["codeQuality", "followStandard", "introduction"]},
{week: "3"},
  {name: "OOP: Intro"},
    {heading: "OOP: Classes and Objects"},
      {location: ["oop", "introduction", "what"]},
      {location: ["oop", "objects", "what"]},
      {location: ["oop", "classes", "what"]},
      {location: ["oop", "objects", "abstraction"]},
      {location: ["oop", "objects", "encapsulation"]},
  {name: "OOP in Java"},
    {heading: "Java: Objects"},
      {location: ["cppToJava", "objects", "usingObjects"]},
      {location: ["cppToJava", "objects", "instanceMembers"]},
      {location: ["cppToJava", "objects", "passingObjects"]},
      {location: ["cppToJava", "objects", "garbageCollection"]},
    {heading: "Java: Classes"},
      {location: ["cppToJava", "classes", "definingClasses"]},
      {location: ["cppToJava", "classes", "gettersAndSetters"]},
    {heading: "OOP, Java: Class-Level Members"},
      {location: ["oop", "classes", "classLevelMembers"]},
      {location: ["cppToJava", "classes", "classLevelMembers"]},
    {heading: "Java: Useful Classes"},
      {location: ["reuse", "apis", "what"]},
      {location: ["cppToJava", "usefulClasses", "api"]},
      {location: ["cppToJava", "usefulClasses", "stringClass"]},
      {location: ["cppToJava", "usefulClasses", "wrapperClasses"]},
      {location: ["cppToJava", "usefulClasses", "arraysClass"]},
      {location: ["cppToJava", "usefulClasses", "scannerClass"]},
  {name: "Implementation"},
    {heading: "Code Quality: Naming"},
      {location: ["codeQuality", "nameWell", "introduction"]},
      {location: ["codeQuality", "nameWell", "basic", "nounsAndVerbsAsNames"]},
      {location: ["codeQuality", "nameWell", "basic", "useStandardWords"]},
      {location: ["codeQuality", "nameWell", "intermediate", "useNameExplain"]},
      {location: ["codeQuality", "nameWell", "intermediate", "notTooLongNorShort"]},
      {location: ["codeQuality", "nameWell", "intermediate", "avoidMisleadingNames"]},
  {name: "Revision Control"},
    {heading: "RCS: Using History"},
      {location: ["revisionControl", "usingHistory"]},
      {location: ["gitAndGithub", "checkout"]},
      {location: ["gitAndGithub", "tag"]},
      {location: ["gitAndGithub", "stash"]},
    {heading: "RCS: Pull, Push"},
      {location: ["gitAndGithub", "pull"]},
      {location: ["gitAndGithub", "push"]},
{week: "4"},
  {name: "OOP + Java"},
    {heading: "OOP + Java: Inheritance"},
      {location: ["oop", "inheritance", "what"]},
      {location: ["oop", "inheritance", "overloading"]},
      {location: ["oop", "inheritance", "overriding"]},
      {location: ["cppToJava", "inheritance", "basic"]},
      {location: ["cppToJava", "inheritance", "objectClass"]},
    {heading: "OOP + Java: Polymorphism"},
      {location: ["oop", "polymorphism", "what"]},
      {location: ["oop", "inheritance", "substitutability"]},
      {location: ["oop", "inheritance", "dynamicAndStaticBinding"]},
      {location: ["oop", "polymorphism", "how"]},
      {location: ["cppToJava", "inheritance", "polymorphism"]},
    {heading: "Java: Constants"},
      {location: ["cppToJava", "misc", "constants"]},
    {heading: "OOP + Java: Enumerations"},
      {location: ["oop", "classes", "enumerations"]},
      {location: ["cppToJava", "misc", "enums"]},
  {name: "Implementation"},
    {heading: "Code Quality: Readability"},
      {location: ["codeQuality", "maximiseReadability", "introduction"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidLongMethods"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidDeepNesting"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidComplicatedExpressions"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidMagicNumbers"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "makeCodeObvious"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "structureCodeLogically"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "dontTripReader"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "practiceKISSing"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "avoidPrematureOptimizations"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "slapHard"]},
      {location: ["codeQuality", "maximiseReadability", "advanced", "makeHappyPathProminent"]},
    {heading: "Code Quality: Refactoring"},
      {location: ["refactoring", "what"]},
      {location: ["intellij", "refactoring"]},
      {location: ["refactoring", "how"]},
      {location: ["refactoring", "when"]},
  {name: "Testing"},
    {heading: "Automated Testing of Text UIs"},
      {location: ["testing", "introduction", "what"]},
      {location: ["testing", "testingTypes", "regressionTesting", "what"]},
      {location: ["testing", "testAutomation", "what"]},
      {location: ["testing", "testAutomation", "testingTextUis"]},
{week: "5"},
  {name: "OOP + Java"},
    {heading: "Java: Casting"},
      {location: ["cppToJava", "misc", "casting"]},
    {heading: "OOP + Java: Abstract Classes"},
        {location: ["oop", "inheritance", "abstractClasses"]},
        {location: ["cppToJava", "inheritance", "abstractClassesAndMethods"]},
    {heading: "OOP + Java: Interfaces"},
        {location: ["oop", "inheritance", "interfaces"]},
        {location: ["cppToJava", "inheritance", "interfaces"]},
    {heading: "Java: Packages"},
      {location: ["cppToJava", "misc", "packages"]},
    {heading: "Java: Access Modifiers"},
      {location: ["cppToJava", "misc", "accessModifiers"]},
  {name: "Implementation"},
    {heading: "Error Handling: Exceptions"},
      {location: ["errorHandling", "introduction", "what"]},
      {location: ["errorHandling", "exceptions", "what"]},
      {location: ["errorHandling", "exceptions", "how"]},
      {location: ["cppToJava", "exceptions", "what"]},
      {location: ["cppToJava", "exceptions", "how"]},
      {location: ["errorHandling", "exceptions", "when"]},
  {name: "Requirements"},
    {heading: "Specifying Requirements [quick peek ahead]"},
      {subheading: "User Stories"},
        {location: ["specifyingRequirements", "userStories", "introduction"]},
        {location: ["specifyingRequirements", "userStories", "details"]},
        {location: ["specifyingRequirements", "userStories", "usage"]},
      {subheading: "Feature Lists"},
        {location: ["specifyingRequirements", "featureList", "what"]},
  {name: "Project Management"},
    {heading: "RCS: Branching, Pull Requests"},
      {location: ["revisionControl", "branching"]},
      {location: ["gitAndGithub", "branch"]},
      {location: ["gitAndGithub", "createPRs"]},
{week: "6"},
  {name: "Java"},
    {heading: "Java: Generics"},
      {location: ["cppToJava", "generics", "what"]},
      {location: ["cppToJava", "generics", "how"]},
    {heading: "Java: Collections"},
      {location: ["cppToJava", "collections", "what"]},
      {location: ["cppToJava", "collections", "arrayListClass"]},
      {location: ["cppToJava", "collections", "hashMapClass"]},
    {heading: "Java: File Access"},
      {location: ["cppToJava", "misc", "fileAccess"]},
    {heading: "Java: JAR Files"},
      {location: ["cppToJava", "misc", "jar"]},
    {heading: "Java: Varargs"},
      {location: ["cppToJava", "misc", "varargs"]},
    {heading: "Java: streams"},
      {location: ["cppToJava", "misc", "streams"]},
  {name: "Requirements"},
    {heading: "Requirements: Intro"},
      {location: ["requirements", "introduction"]},
      {location: ["requirements", "nonFunctionalRequirements"]},
      {location: ["requirements", "prioritizing"]},
      {location: ["requirements", "quality"]},
    {heading: "Requirements: Gathering"},
      {location: ["gatheringRequirements", "brainstorming"]},
      {location: ["gatheringRequirements", "productSurveys"]},
      {location: ["gatheringRequirements", "observation"]},
      {location: ["gatheringRequirements", "userSurveys"]},
      {location: ["gatheringRequirements", "interviews"]},
      {location: ["gatheringRequirements", "focusGroups"]},
      {location: ["gatheringRequirements", "prototyping"]},
    {heading: "Requirements: Specifying [continued from last week]"},
      {subheading: "Prose"},
        {location: ["specifyingRequirements", "prose", "what"]},
      {subheading: "User Stories [Repeated from last week]"},
        {location: ["specifyingRequirements", "userStories", "introduction"]},
        {location: ["specifyingRequirements", "userStories", "details"]},
        {location: ["specifyingRequirements", "userStories", "usage"]},
      {subheading: "Feature Lists [Repeated from last week]"},
        {location: ["specifyingRequirements", "featureList", "what"]},
      {subheading: "Use Cases"},
        {location: ["specifyingRequirements", "useCases", "introduction"]},
      {subheading: "Glossary"},
        {location: ["specifyingRequirements", "glossary", "what"]},
      {subheading: "Supplementary Requirements"},
        {location: ["specifyingRequirements", "supplementaryRequirements", "what"]},
  {name: "Implementation"},
    {heading: "IDEs: Intermediate Features"},
      {location: ["ides", "debugging", "what"]},
      {location: ["intellij", "debuggingBasic"]},
      {location: ["intellij", "productivityShortcuts"]},
  {name: "Project Management"},
    {heading: "RCS: Doing more with Branches and PRs"},
      {location: ["gitAndGithub", "mergeConflicts"]},
      {location: ["gitAndGithub", "managePRs"]},
    {heading: "Code Quality: Unsafe Practices"},
      {location: ["codeQuality", "avoidShortcuts", "introduction"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "useDefaultBranch"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "dontRecycleVarsOrParams"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "avoidEmptyCatchBlocks"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "deleteDeadCode"]},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseVariableScope"]},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseCodeDuplication"]},
{week: "7"},
  {name: "Java"},
    {heading: "Java: JavaFX"},
      {location: ["cppToJava", "misc", "javaFX"]},
  {name: "Documentation"},
    {heading: "Documentation Tools"},
      {subheading: "Javadoc"},
        {location: ["documentation", "tools", "javaDoc", "what"]},
        {location: ["documentation", "tools", "javaDoc", "how"]},
      {subheading: "Markdown"},
        {location: ["documentation", "tools", "markdown", "what"]},
        {location: ["documentation", "tools", "markdown", "how"]},
      {subheading: "AsciiDoc"},
        {location: ["documentation", "tools", "asciiDoc", "what"]},
  {name: "Implementation"},
    {heading: "Code Quality: Code Comments"},
      {location: ["codeQuality", "commentMinimally", "introduction"]},
      {location: ["codeQuality", "commentMinimally", "basic", "dontRepeatObvious"]},
      {location: ["codeQuality", "commentMinimally", "basic", "writeToReader"]},
      {location: ["codeQuality", "commentMinimally", "intermediate", "explainWhatWhyNotHow"]},
  {name: "Project Management"},
    {heading: "SDLC Process Models: Basics"},
      {location: ["processModels", "introduction", "what"]},
      {location: ["processModels", "introduction", "sequentialModels"]},
      {location: ["processModels", "introduction", "iterativeModels"]},
    {heading: "Continuous Integration/Deployment"},
      {location: ["integration", "introduction", "what"]},
      {location: ["integration", "buildAutomation", "what"]},
      {location: ["integration", "buildAutomation", "continuousIntegrationDeployment"]},
    {heading: "RCS: Workflows"},
      {location: ["revisionControl", "forkingWorkflow"]},
      {location: ["gitAndGithub", "forkingWorkflow"]},
      {location: ["revisionControl", "drcsVsCrcs"]},
      {location: ["revisionControl", "featureBranchFlow"]},
      {location: ["revisionControl", "centralizedFlow"]},
{week: "8"},
  {name: "Quality Assurance"},
    {heading: "Developer Testing"},
      {location: ["testing", "testingTypes", "developerTesting", "what"]},
      {location: ["testing", "testingTypes", "developerTesting", "why"]},
      {location: ["testing", "testAutomation", "usingTestDrivers"]},
      {location: ["testing", "testAutomation", "tools"]},
      {location: ["cppToJava", "junit", "basic"]},
  {name: "Documentation"},
    {heading: "Writing Developer Documents"},
      {location: ["documentation", "introduction", "what"]},
  {name: "Design"},
    {heading: "Design: Models"},
      {location: ["design", "introduction", "what"]},
      {location: ["modeling", "introduction", "what"]},
      {location: ["modeling", "introduction", "how"]},
    {heading: "Class/Object Diagrams: Basics"},
      {location: ["modeling", "modelingStructures", "ooStructures"]},
      {location: ["modeling", "modelingStructures", "classDiagramsBasic"]},
      {location: ["modeling", "modelingStructures", "objectDiagrams"]},
      {location: ["uml", "miscellaneous", "objectVsClassDiagrams"]},
      {location: ["uml", "classDiagrams", "associationsAsAttributes", "what"]},
      {location: ["uml", "notes", "notes"]},
  {name: "Project Management"},
    {heading: "Project Mgt: Scheduling and Tracking"},
      {location: ["projectPlanning", "milestones"]},
      {location: ["projectPlanning", "buffers"]},
      {location: ["projectPlanning", "issueTrackers"]},
      {location: ["projectPlanning", "workBreakdownStructure"]},
      {location: ["projectPlanning", "ganttCharts"]},
      {location: ["projectPlanning", "pertCharts"]},
      {location: ["teamwork", "teamStructures"]},
{week: "9"},
  {name: "Documentation"},
    {heading: "Class Diagrams: Intermediate-Level"},
      {location: ["modeling", "modelingStructures", "classDiagramsIntermediate"]},
  {name: "Implementation"},
    {heading: "Logging"},
      {location: ["errorHandling", "logging", "what"]},
      {location: ["errorHandling", "logging", "how"]},
    {heading: "Assertions"},
      {location: ["errorHandling", "assertions", "what"]},
      {location: ["errorHandling", "assertions", "how"]},
      {location: ["errorHandling", "assertions", "when"]},
  {name: "Design"},
    {heading: "Design Principles"},
      {subheading: "Abstraction"},
        {location: ["designFundamentals", "abstraction", "what"]},
      {subheading: "Coupling"},
        {location: ["designFundamentals", "coupling", "what"]},
        {location: ["designFundamentals", "coupling", "how"]},
        {location: ["designFundamentals", "coupling", "types"]},
      {subheading: "Cohesion"},
        {location: ["designFundamentals", "cohesion", "what"]},
        {location: ["designFundamentals", "cohesion", "how"]},
      {subheading: "Some other principles"},
        {location: ["principles", "singleResponsibilityPrinciple"]},
        {location: ["principles", "separationOfConcernsPrinciple"]},
  {name: "Quality Assurance"},
    {heading: "Testing: Intermediate Techniques"},
      {location: ["testing", "introduction", "testability"]},
      {location: ["cppToJava", "junit", "intermediate"]},
      {location: ["testing", "tdd", "what"]},
{week: "10"},
  {name: "Documentation"},
    {heading: "Sequence Diagrams: Basics"},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsBasic"]},
    {heading: "Sequence Diagrams: Intermediate-Level"},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsIntermediate"]},
      {location: ["uml", "sequenceDiagrams", "parallelPaths"]},
      {location: ["uml", "sequenceDiagrams", "referenceFrames"]},
  {name: "Design"},
    {heading: "Design Patterns"},
      {subheading: "Introduction"},
        {location: ["designPatterns", "introduction", "what"]},
        {location: ["designPatterns", "introduction", "format"]},
      {subheading: "Singleton pattern"},
        {location: ["designPatterns", "singleton", "what"]},
        {location: ["designPatterns", "singleton", "implementation"]},
        {location: ["designPatterns", "singleton", "evaluation"]},
      {subheading: "Facade pattern"},
        {location: ["designPatterns", "facade", "what"]},
  {name: "Quality Assurance"},
    {heading: "Testing: Test Coverage"},
      {location: ["testing", "testCoverage", "what"]},
      {location: ["testing", "testCoverage", "how"]},
{week: "11"},
  {name: "Design"},
    {heading: "Architecture"},
      {subheading: "Introduction"},
        {location: ["designApproaches", "multilevelDesign", "what"]},
        {location: ["architecture", "introduction", "what"]},
        {location: ["architecture", "architectureDiagrams", "reading"]},
      {subheading: "Architectural Styles"},
        {location: ["architecture", "architecturalStyles", "introduction", "what"]},
        {location: ["architecture", "architecturalStyles", "nTier", "what"]},
        {location: ["architecture", "architecturalStyles", "clientServer", "what"]},
  {name: "Quality Assurance"},
    {heading: "Types of Testing"},
      {subheading: "Unit Testing"},
        {location: ["testing", "testingTypes", "unitTesting", "what"]},
        {location: ["testing", "testingTypes", "unitTesting", "stubs"]},
        {location: ["testing", "dependencyInjection", "what"]},
        {location: ["testing", "dependencyInjection", "how"]},
      {subheading: "Integration Testing"},
        {location: ["testing", "testingTypes", "integrationTesting", "what"]},
        {location: ["testing", "testingTypes", "integrationTesting", "how"]},
      {subheading: "System Testing"},
        {location: ["testing", "testingTypes", "systemTesting", "what"]},
        {location: ["testing", "testAutomation", "testingGuis"]},
      {subheading: "Acceptance Testing"},
        {location: ["testing", "testingTypes", "acceptanceTesting", "what"]},
        {location: ["testing", "testingTypes", "acceptanceTesting", "acceptanceVsSystemTesting"]},
      {subheading: "Alpha/Beta Testing"},
        {location: ["testing", "testingTypes", "alphaBetaTesting", "what"]},
    {heading: "Test Case Design"},
      {location: ["testCaseDesign", "introduction", "what"]},
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "what"]},
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "when"]},
      {location: ["testCaseDesign", "introduction", "positiveVsNegative"]},
      {location: ["testCaseDesign", "introduction", "blackVsGlass"]},
      {location: ["testCaseDesign", "more", "testingUseCases"]},
    {heading: "Equivalence Partitioning"},
      {location: ["testCaseDesign", "equivalencePartitions", "what"]},
      {location: ["testCaseDesign", "equivalencePartitions", "basic"]},
      {location: ["testCaseDesign", "equivalencePartitions", "intermediate"]},
{week: "12"},
  {name: "Quality Assurance"},
    {heading: "Boundary Value Analysis"},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "what"]},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "how"]},
    {heading: "Combining Multiple Test Inputs"},
      {location: ["testCaseDesign", "combiningTestInputs", "why"]},
      {location: ["testCaseDesign", "combiningTestInputs", "combinationStrategies"]},
    {heading: "Other QA Techniques"},
      {location: ["qualityAssurance", "introduction", "what"]},
      {location: ["qualityAssurance", "introduction", "validationVsVerification"]},
      {location: ["qualityAssurance", "codeReviews", "what"]},
      {location: ["qualityAssurance", "staticAnalysis", "what"]},
      {location: ["qualityAssurance", "formalVerification", "what"]},
  {name: "Project Management"},
    {heading: "SDLC Process Models: XP/Scrum"},
      {location: ["processModels", "introduction", "agileModels"]},
      {location: ["processModels", "exampleProcessModels", "scrum"], evidence: "project.md#relate_process"},
      {location: ["processModels", "exampleProcessModels", "xp"], evidence: "project.md#relate_process"},
{week: "13"}
]%}

{% macro show_week_pagetop(week_num, category) %}

{% set week = weeks[week_num - 1] %}

{% set categories = {
  notices: {name: "Summary", file: "index", icon: icon_announcement, pagenav: 4},
  topics: {name: "Topics", file: "topics", icon: icon_book, pagenav: 3},
  project: {name: "Project", file: "project", icon: icon_project, pagenav: 4},
  tutorial: {name: "Tutorial", file: "tutorial", icon: icon_tutorial, pagenav: 4},
  admin: {name: "Admin Info", file: "admin", icon: icon_info, pagenav: 4}
} %}

<frontmatter>
title: "Week {{ week.num }} - {{ categories[category].name }}"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: {{ categories[category].pagenav }}
</frontmatter>

<nav>
<ul class="pagination mt-2">
{%- set previous_status = " disabled" if week_num == 1 else "" -%}
{%- set next_status = " disabled" if week_num == 13 else "" -%}
<li class="page-item{{ previous_status }}"><a class="page-link" href="../week{{ (week_num - 1) }}/"><md>:glyphicon-chevron-left: **Previous Week**</md></a></li>
<li class="page-item">&nbsp;&nbsp;&nbsp;</li>
{% for c,v in categories %}
  {%- set is_active = " active" if categories[category] == v else "" -%}
  <li class="page-item{{ is_active }}"><a class="page-link" href="{{v.file}}.html">{{ v.icon }} {{v.name}}</a></li>
</li>
{% endfor %}
<li class="page-item">&nbsp;&nbsp;&nbsp;</li><li class="page-item{{ next_status }}"><a class="page-link" href="../week{{ (week_num + 1) }}/"><md>**Next Week** :glyphicon-chevron-right:</md></a></li>
</ul>
</nav>

<p/>

# Week {{ week.num }} <small><small>%%[{{ week.day }}]%% - {{ categories[category].name }}</small></small>

{% endmacro %}


{% macro show_week_summary(week_num) %}

<span id="summary">
<div class="container">
  <div class="row">
  <div class="col-sm border-right border-bottom">

{% if week_num != 1 %}
{{ topics.show_week_schedule_main(week_num, all_topics, "", is_toc=true, is_flat=true) }}

<panel type="seamless" header="%%Full ToC%%">
  <include src="topics.md#toc" optional />
</panel>
{% endif %}
  </div>
  <div class="col-sm border-bottom">

**Admin:**
<include src="admin.md#summary" optional/>
<include src="project-{{ module | lower }}.mbdf#summary" optional/>

  </div>
  </div>
</div>
</span>
<br>
{% endmacro %}

{% macro show_project_summary(ip_file=false, tp_file=false, milestone=false) %}
<div id="summary" class="lead border-bottom border-left ml-3 mb-3 pl-2" style="color: purple;">

{% if ip_file %}
**iP:**
<include src="../../admin/{{ ip_file }}#summary" />
{% endif %}
{% if tp_file %}
**tP:** {% if milestone %}<span class="border rounded text-success border-success pr-1 pl-1">:fas-tag: **{{ milestone }}**</span>{% endif %}
<include src="../../admin/{{ tp_file }}#summary" />
{% endif %}
</div>

{% endmacro %}


{% macro show_week_index_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "notices") }}

<include src="notices-{{ module | lower }}.mbdf" optional />

{{ show_week_summary(week_num) }}
</div>
{% endmacro %}


{% macro show_week_admin_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "admin") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Admin info relevant to the week will appear in this tab.
</box>
{% endif %}

{{ show_weekly_admin_tasks(week_num) }}
</div>
{% endmacro %}


{% macro show_week_topics_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "topics") }}

{% if week_num == "1" %}
<box type="info" dismissible>

* Topics allocated to the week will appear in this tab.
* If the lecture is in the 2nd half of the week (i.e., Wednesday 12 noon or later), the lecture in week `N` will cover topics allocated to the week `N+1` e.g., **Lecture 1 will cover Week 2 topics**, and so on.
</box>
{% endif %}
{{ topics.show_week_schedule(week_num, all_topics) }}
</div>
{% endmacro %}


{% macro show_week_tutorial_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "tutorial") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Information relevant to the week's tutorial will appear in this tab.
</box>
{% endif %}
<include src="tutorial-{{ module | lower }}.mbdf" optional />
</div>
{% endmacro %}


{% macro show_week_project_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "project") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Project-related information relevant to the week will appear in this tab.
</box>
{% endif %}
<include src="project-{{ module | lower }}.mbdf" optional />
</div>
{% endmacro %}


<!-- ============================= page content ============================================ -->

{% set week_to_show = "1" if current_week in ["-1", "0", "14", "15"] else current_week %}
<include src="week{{ week_to_show }}/index.md" />
