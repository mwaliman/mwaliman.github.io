---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects

{:.lead}
Here are some projects I have worked on for school, work, or fun. Watch this space!
<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
