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
#image:
#  feature: chalk.png
#  credit: Five Sixteenths
#  creditlink: http://www.fivesixteenthsblog.com/2012_12_01_archive.html
---


{% for clip in site.data.clips %}
  <h3><a href="{{clip.url}}" target="_blank">{{clip.title}}</a></h3>
  <figure class="half">     
     <a href="http://0.0.0.0:4000/images/{{clip.image}}">
        <img src="http://0.0.0.0:4000/images/{{clip.image}}"></a>
        <figcaption><a style="text-decoration: underline" href="{{clip.url}}" target="_blank">Published on {{clip.date}}</a> <p> {{clip.description}} <a href="{{clip.url}}" target="_blank">Read the clip</a></p></figcaption>     
  </figure>
  <hr />
{% endfor %}

