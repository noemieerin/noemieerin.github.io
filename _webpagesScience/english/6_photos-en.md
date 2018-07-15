---
layout: page
title: Photos
description: pictures speak louder than words
lang: english
link: photos
img: /img/soleil1.jpg
permalink: /en/science/photos/
exclude: true
---
<div class="header-bar">
  <h1>*Photos</h1>
  <hr>
</div>


{% assign projects=site.webpagesPhotos | where: "lang", page.lang %}
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
