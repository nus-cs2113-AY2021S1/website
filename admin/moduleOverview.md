{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("moduleOverview") %} 
<div id="main">

<big><p class="lead text-secondary">An iterative introduction to Software Engineering...</p></big>

<img src="{{baseUrl}}/images/growingPlant.png" width="700">

<p class="lead"><md>{{ module_pair }} is an introductory Software Engineering module covering **a balance of basic SE theory and practical skills** needed to work in a project that has a software component. The module follows an <tooltip content="going through SE topics several times while increasing depth, as opposed to going through topics sequentially">**iterative approach**</tooltip> to covering topics. The module also introduces you to the Java programming language, the OOP paradigm, and some basic UML models.</md></p>

* **The theory side** of this module is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this module website.

* **On the practice side**, you will first ramp up your technical skills by doing a small individual project in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). Then, you will move to a team project in which you will build another small <tooltip content="Comman Line Interface">CLI</tooltip> app while working as a team.


<panel src="appendixC-faq.md#admin-faq-tVsNonT" header="Admin {{ icon_embedding }} **FAQ: What are the differences between {{ module }} and {{ module }}T?**" class="embedding" minimized />

</div>

{% endcall %}
