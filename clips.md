---
layout: page
permalink: /clips.html
tagline: Tom Meagher
tags: [about]
title: Apps, maps, edits and clips
Date: 2014-03-30 08:32
Author: Tom
Slug: clips
Modified: 2014-03-30
image:
  feature: chips.png
  credit: Texture Palace
  creditlink: http://www.texturepalace.com/wp-content/uploads/computer-texture-medium-8.jpg
---

*You can read many of my recent stories at [The Marshall Project's website](https://www.themarshallproject.org/staff/tom-meagher).*

{% for clip in site.data.clips %}
  <h3><a href="{{clip.url}}" target="_blank">{{clip.title}}</a></h3>
  <figure>     
     <a href="{{ site.url }}/images/{{clip.image}}">
        <img src="{{ site.url }}/images/{{clip.image}}"></a>
        <figcaption><a style="text-decoration: underline" href="{{clip.url}}" target="_blank">Published on {{clip.date}}</a> <p> {{clip.description}} <a href="{{clip.url}}" target="_blank">Read the clip</a></p></figcaption>     
  </figure>
  <hr />
{% endfor %}
