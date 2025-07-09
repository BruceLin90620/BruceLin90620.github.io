---
layout: page
title: About
permalink: /about/
weight: 1
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
I am a Master's student at Purdue University with a focus on embedded systems. This interest is built on extensive hands-on robotics experience, where I developed complete autonomous navigation systems for industrial partners, leading projects from simulation all the way to final hardware deployment.


---

## Education
<div class="row">
  <div class="col mt-4">
    <div class="timeline-body bg-themed">
      {% for item in site.data.timeline.education %}
        <div class="timeline-item">
          <div class="content">
            <h3>{{ item.title }}</h3>
            <h5 class="date">{{ item.location }} • {{ item.from }} — {{ item.to }}</h5>
            <p>{{ item.description }}</p>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</div>

<br>

## Experience
<div class="row">
  <div class="col mt-4">
    <div class="timeline-body bg-themed">
      {% for item in site.data.timeline.experience %}
        <div class="timeline-item">
          <div class="content">
            <h3>{{ item.location }}</h3>
            <h5 class="date">{{ item.title }} • {{ item.from }} — {{ item.to }}</h5>
            <p>{{ item.description }}</p>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</div>

---

<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>