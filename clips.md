---
layout: page
permalink: /clips.html
tagline: Tom Meagher
tags: [about]
title: Apps, maps, edits and clips
Date: 2014-03-30 08:32
Author: Tom
Slug: clips
Modified: 2021-02-20
image:
  feature: chips.png
  credit: Texture Palace
  creditlink: http://www.texturepalace.com/wp-content/uploads/computer-texture-medium-8.jpg
---

*Read my recent stories at **[The Marshall Project](https://www.themarshallproject.org/staff/tom-meagher)** and see the data and code behind them **[on Github](https://github.com/themarshallproject/)**.*

{% for clip in site.data.clips %}
  <h3><a href="{{clip.url}}" target="_blank">{{clip.title}}</a></h3>
  <figure>     
     <a href="{{ site.url }}/images/{{clip.image}}">
        <img src="{{ site.url }}/images/{{clip.image}}"></a>
        <figcaption><a style="text-decoration: underline" href="{{clip.url}}" target="_blank">Published on {{clip.date}}</a> <p> {{clip.description}} <a href="{{clip.url}}" target="_blank">Read the clip</a></p></figcaption>     
  </figure>
  <hr />
{% endfor %}

