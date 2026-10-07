---
layout: default
title: Sebastian Mostek
---

## Welcome


![Profile Picture]({{ "assets/images/Professional_PFP.jpg" | relative_url }}){: class="profile-image"}

 
My name is {{ site.name }}, and I'm a young Mechanical Engineer and Cornell graduate looking for a job focused on public good. 

I have always tried to be a generalist, both within engineering and more broadly. If I can be said to have an area of true expertise it is in pure math and physics, which has proven especially useful in helping me to quickly learn new technical fields.

This site serves to catalogue and present the many projects I've worked on and skills I've learned, as well as being a digital home for <a href="{{ "/cv/" | relative_url }}">my resume</a>. 

For a pdf of mostly the same portfolio content as this site, click [here]({{ "assets/SMostek_Technical_Portfolio.pdf" | relative_url }}).

### Professional Experience
<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.jobs %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p>{{ project.title}}</p>
        </a>
      </div>
    {% endfor %}
</div>
</div>

### Projects & Coursework
<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p>{{ project.title}}</p>
        </a>
      </div>
    {% endfor %}
</div>
</div>
