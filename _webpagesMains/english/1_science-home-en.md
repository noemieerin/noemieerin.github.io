---
layout: page
title: science
lang: english
link: science-home
permalink: /en/science/
exclude: true
---

<div class="header-bar">
  <h1>*Noémie Erin</h1>
  <h3>evolutionary biologist</h3>
  <hr>
</div>


{% assign projects=site.webpagesScience | where: "lang", page.lang %}
{% for project in projects %}

{% if project.redirect %}
<div class="project">
    <div class="circular">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="circular" src="{{ project.img }}"/>
        {% else %}
        <div class="circular blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="circular">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="circular" src="{{ project.img }}"/>
        {% else %}
        <div class="circular blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
