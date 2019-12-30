{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("moduleExpectations") %} 
<div id="main">

### Workload

As 60% of this module is based on CA, it can appear to be _heavy_. However, **it is not expected that you will spend more time on this module than its <tooltip content="e.g., if this module is core for you, it should not take more time than other level 2 core modules in your program">peer modules</tooltip>**. 
* Note that the **module contains more things than a typical students can do**, in order to provide enough things for even the strongest students to learn as much as they wish to. 
* This means it is ==**perfectly OK if you don't have time to learn everything the module offers**==. Control your workload based on time you spend for the module in a week e.g., 1-1.5 days per week.
* We have provided a star rating system to guide you when prioritizing which things to do.

<div id="starRatingSystem">

#### Star Rating System

<div class="indented">

<p class="lead"><md>We use a _star rating system_ indicate the importance of module components. **Start with things that are rated one-star and progress to things with more stars.** Things rated four stars are optional.</md></p>

**Star ratings for topics** (and textbook sections):

* **One-star topics** {{ one_star }} are essential to keep up with the module. We recommend you to ==learn these topics if you want to pass the module== (i.e. up to a **C** grade).
* **Two-stars topics** {{ two_stars }} can get you up to a **B+**.
* **Three-stars topics** {{ three_stars }} can get you up to an **A**.
* **Four-stars topics** {{ four_stars }} can push you beyond the limits of the module, and help you get into a level above those who merely limit themselves to the topics of the module. They ==are not examinable==.

**Star ratings for other things** e.g., admin info sections:

* The module uses a similar star rating system to indicate the importance of other info in this website. i.e., information rated as one-star are the most essential. ==Info rated four stars are non-essential and can be ignored== without affecting your ability to follow the module.

</div>
</div>

</div>

{% endcall %}
