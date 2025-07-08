---
layout: page
title: About
permalink: /about/
weight: 1
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
I graduated from the Department of Mechanical Engineering at National Taipei University of Technology. Currently, I am a researcher at City Science Lab, where my primary focus is on Robotics. My work involves developing innovative robots and integrating various cutting-edge technologies for applications in factories and urban environments.


---

## Experience
<div class="row">
  <div class="col mt-4">
    <div class="timeline-body bg-themed">
      {% for item in site.data.timeline.experience %}
        <div class="timeline-item">
          <div class="content">
            <h2>{{ item.location }}</h2>
            <h6 class="date">{{ item.title }} • {{ item.from }} — {{ item.to }}</h6>
            {% for project in item.projects %}
              <div style="margin-top: 1rem;">
                <h5>{{ project.name }}</h5>
                {% if project.star.situation and project.star.situation != "" %}
                  <p>{{ project.star.situation }} {{ project.star.task }}</p>
                {% endif %}
                <ul>
                  {% for action_item in project.star.action %}
                    <li>{{ action_item }}</li>
                  {% endfor %}
                </ul>
                {% if project.star.result and project.star.result != "" %}
                  <p><strong><i class="fas fa-chart-line"></i> Key Achievement:</strong> {{ project.star.result }}</p>
                {% endif %}
              </div>
            {% endfor %}
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</div>

<br>

## Education
<div class="row">
  <div class="col mt-4">
    <div class="timeline-body bg-themed">
      {% for item in site.data.timeline.education %}
        <div class="timeline-item">
          <div class="content">
            <h2>{{ item.title }}</h2>
            <h6 class="date">{{ item.location }} • {{ item.from }} — {{ item.to }}</h6>
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