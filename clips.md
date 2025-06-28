---
layout: page
permalink: /clips.html
tagline: Tom Meagher
tags: [about]
title: Selected clips and honors
Date: 2024-10-14 08:32
Author: Tom
Slug: clips
Modified: 2021-02-20
#image:
#  feature: chips.png
#  credit: Texture Palace
#  creditlink: http://www.texturepalace.com/wp-content/uploads/computer-texture-medium-8.jpg
---
## My editing and producing

{% for clip in site.data.editing_clips %}
  <a href="{{clip.url}}" style="color: blue" target="_blank">{{clip.title}}</a><br />
  {{clip.description}}
  {% if clip.awards %}Honored with {{clip.awards}}{% endif %}
<p><br /></p>  
{% endfor %}

## My reporting

{% for clip in site.data.writing_clips %}
  <a href="{{clip.url}}" style="color: blue" target="_blank">{{clip.title}}</a><br />
  {{clip.description}}
  {% if clip.awards %}Honored with {{clip.awards}}{% endif %}
<p><br /></p>  
{% endfor %}




<!--- original grouping
{% for clip in site.data.editing_clips %}
  <h3><a href="{{clip.url}}" target="_blank">{{clip.title}}</a></h3>
  <figure>     
     <a href="{{ site.url }}/images/{{clip.image}}">
        <img src="{{ site.url }}/images/{{clip.image}}"></a>
        <figcaption><a style="text-decoration: underline" href="{{clip.url}}" target="_blank">Published on {{clip.date}}</a> <p> {{clip.description}}</p></figcaption>     
  </figure>
  <hr />
{% endfor %}
--->


