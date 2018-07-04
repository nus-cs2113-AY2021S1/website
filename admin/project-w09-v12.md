<frontmatter>
title: "Admin: Project → v1.2 [week 9]"
footer: footer.md
siteNav: adminSiteNav.md
</frontmatter>

<link rel="stylesheet" href="../css/main.css">
<link rel="stylesheet" href="../css/admin.css">

<include src="../common/header.md" />

<div class="website-content" id="main">

<div id="title">

## Project → v1.2 [week 9]
</div>
<div id="body">

<tip-box>

Overview: <include src="project-deliverables.md#v12-overview" inline />
</tip-box> 

**v1.2 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
:bust_in_silhouette: Contributed code to the product as described in mid-v1.2 progress guide | some code merged
:bust_in_silhouette: Described implementation details in the Developer Guide | some text and some diagrams added to the developer guide (at least in a PR), comprising at least one page worth of content
:busts_in_silhouette: v1.2 managed using GitHub features (issue tracker, milestones, etc.) | A new version git tagged `v1.2` is in your repo.<br> There is evidence of an attempt (even if not completely successful) to use GitHub features as described in <trigger trigger="click" for="modal:v12-projectTracking">[Admin {{ icon_embedding }} Appendix E: GitHub: Project Schedule Tracking]</trigger>. 

  
### v1.2 Project Management

* :busts_in_silhouette: Manage, and close, the v1.2 milestone using GitHub.

### v1.2 Product

* :bust_in_silhouette: Merge some code into master (in the team repo).  

<tip-box> 

:bulb: We use a tool called _Collate_ to extract out code written by each member in your final project submission. The tool requires you to annotate code with special tags to mark code written by you. Adding those annotations is usually done at v1.3 but you are welcome to start early. 

<panel header="**How to collate code for grading**" no-close>
  <include src="collate.md" />
</panel><p/>

</tip-box>

### v1.2 Documentation

* **User Guide**: Update as necessary.
  * If a feature has been released in this version, replace the `Coming in v2.0` annotation with a `Since v1.2`. Also replace UI mock-ups with actual screenshots.
  * If a feature design has changed, update the descriptions accordingly.

* **Developer Guide**:
  * ==Each member should describe the implementation of at least one enhancement she has added== (or planning to add). <br>
    Expected length: 1+ page per person
  * The description can contain things such as,
    * How the feature is implemented.
    * Why it is implemented that way.
    * Alternatives considered.
  * The stated objective is to explain the implementation to a future developer, but a hidden objective is to show evidence that you can document deeply-technical content using prose, examples, diagrams, code snippets, etc. appropriately. To that end, you may also describe features that you plan to implement in the future, even beyond v1.4 (hypothetically).
  * For an example, see [the description of the undo/redo feature implementation in the AddressBook-Level4 developer guide](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/DeveloperGuide.html#undo-redo-mechanism).
  

### v1.2 Demo

Do an informal demo of the new feature during the tutorial. ==Each team member should demo their own work, using commit tagged as `v1.2` in the `master` branch== %%&nbsp;i.e. only features included in the current release should be demoed%%.

</div>
</div>