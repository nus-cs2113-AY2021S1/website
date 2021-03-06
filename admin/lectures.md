{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("lectures") %}
<div id="main">

<img src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%">

****Timing/venue****:

<include src="../_module-{{ module | lower }}/timetables.mbdf#lectures-s{{ S }}" inline />

<div tags="m--tic4001" class="indented">

**The lecture+tutorial slot ({{ day_lecture }} 6.30pm-9.30pm) will be repurposed** as follows, due to this being a 100% project module:

* **6.30-7pm**: No formal activities. Work with team members and consult instructors if you need help with the previous week's tasks.
* **7-7.30pm**: Weekly briefing.
* **7-30-9.30pm**: Do the lecture activities (if any) or work with team members to do weekly project activities. The tutor will observe or get involved in your team's work as necessary. You may approach instructors for help during this period.
</div>

<div tags="m--cs2103 m--cs2113">

Lectures start on time sharp and end around 15 minutes before official end time.
</div>

****Mode****:
* Will be done using Zoom. More information coming soon.

<div tags="m--cs2103 m--tic4001">

* Some topics come with pre-recorded lecture videos.
</div>

<div id="tip-about-lecture-videos" class="indented">

<box type="tip" seamless>

##### Tips for watching lecture videos

* ==You can watch video lectures at faster speeds== (`x1.25` or even `x1.5`) to save time.
* Lecture videos require NUSNET login.
</box>
</div>


****Attendance****: Attendance for the ==first lecture is compulsory==.

****Handouts****: There are no handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in the {{ url_schedule }} (organized by order of coverage).

****Slides****: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to LumiNUS *after* the lecture.

</div>

{% endcall %}
