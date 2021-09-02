---
layout: page
title: "Home"
class: home
---


<div class="columns" markdown="1">

<div class="me" markdown="1">
<picture>
  <source srcset='/images/profhawaii.jpg' />
  <img>
</picture>

{:.no-list}
<!-- * Matthew Waliman  <a href="">CV</a>  
* <a href="mailto:{{ site.email }}"> <i class="fas fa-envelope"></i> {{ site.email }}</a>
 --></div>

<div class="intro" markdown="1">

# Hi, I'm Matthew!

I'm an Electrical and Computer Engineering M.S. student at UCLA.

My research interests are Human Computer Interaction, Graphics and Computer Vision. I did my undergrad at UC Berkeley where I worked with <a href="http://www-video.eecs.berkeley.edu/~avz/">Prof. Avideh Zakhor</a> and <a href="https://people.eecs.berkeley.edu/~bjoern/">Prof. Bjoern Hartmann</a>.

Sometimes I also <a href="https://www.youtube.com/watch?v=Q1qJ6_Uwj4A" target="_blank" rel="noopener noreferrer">sing</a>.
</div>


</div>

<!-- Details are in my [CV]({{ "/cv/" | relative_url }}). -->

<!-- ## Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fa fa-chevron-circle-right"></i>
  Show More Projects
</a> -->

## Publications

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<!-- <a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a> -->

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<!-- <div class="travel" markdown="1">
## Latest Travel

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div> -->

</div>
