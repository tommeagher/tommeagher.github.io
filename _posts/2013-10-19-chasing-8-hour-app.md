---
layout: post
title: Chasing the 8-hour app
Date: 2013-10-19 08:27
Author: Tom
category: blog
Link: /2013/10/hack-jersey-chases-the-8-hour-app.html
Slug: hack-jersey-chases-the-8-hour-app
tags: [Hack Jersey, campaign finance, hackathons, newsapps, open data, Sunlight Foundation, civic hacking]
---
<p><em>Cross-posted from the <a href="http://sunlightfoundation.com/blog/2013/10/11/opengov-voices-chasing-the-8-hour-app/" target="_blank">Sunlight Foundation's OpenGov Voices blog</a>.</em></p>

<p>A few weeks ago, <a title="Hack Jersey" href="http://www.hackjersey.com" target="_blank">Hack Jersey</a> brought a group of journalists and developers together to wrestle with campaign finance data. We thought it would be a good opportunity for many to get their hands dirty and to start thinking about new ways of reporting and building with the data.</p>

<p>In one room of our event at the <a href="http://www.njit.edu/">New Jersey Institute of Technology</a>, a group of journalists went on a data expedition, learning how to explore reports from the state's <a href="http://www.hackjersey.com/2013/09/guiding-journalists-through-strange-world-of-money-and-politics/">Election Law Enforcement Commission</a>. In another, we gathered developers to try to build a campaign finance app for New Jersey using the <a href="http://sunlightfoundation.com/api/">Sunlight Foundation's APIs</a> in a single work session.</p>

<p>We began Hack Jersey about a year ago, starting with some conversations between journalists and developers who wanted to work together to improve news and data in the Garden State. Since then, with the support of the <a href="http://njnewscommons.org/">NJ News Commons</a> and <a href="http://www.mozillaopennews.org/">Knight-Mozilla OpenNews</a>, we sponsored the <a href="http://sunlightfoundation.com/blog/2013/03/29/opengov-voices-hack-jersey-hackathon-public-data-solving-problems/">first news-themed hackathon in New Jersey</a> and several smaller training events.</p>

<p>We've been eager to take the excitement from the traditional hackathon competition and translate it into projects that news organizations and news consumers can actually use. We wanted our <a href="http://www.hackjersey.com/event/law-money-and-politics/">"Law, Money &amp; Politics" hackday</a> to entice developers to work together to solve a news problem instead of competing against one another. We were psyched to be able to use Sunlight's APIs in that effort and to have the support of the foundation, which helped sponsor our event.</p>

<p>There was clearly an interest among developers in this approach. About 15 coders--from computer science programs at local universities, the startup community and nearby news organizations--came to work, and another four helped us plan the project in our pre-hack meetups.</p>

<p>As the group took shape, we needed to figure out what we wanted to build. We spent almost four hours over two weeks talking and thinking about ideas we solicited from local news organizations. What problem did we want our app to solve?</p>

<p>We all agreed that campaign finance is a murky, labyrinthine realm and that people in New Jersey could use all the help they could get understanding it. We love the Sunlight Foundation's <a href="http://data.influenceexplorer.com/api">InfluenceExplorer API and the way it makes</a> state data, cleaned and cared for by the <a href="http://www.followthemoney.org/">National Institute for Money in State Politics</a>, accessible. We could spend a whole hack day or two trying to mold our state ELEC data into a more useful format, but InfluenceExplorer and NIMSP has done a lot of that dirty work for us.</p>

<p>After what we thought was much discussion and tinkering with the <a href="http://tryit.sunlightfoundation.com/influenceexplorer">API</a>, we zeroed in on the idea of comparing campaign donations coming from industries into state elections. What industries were backing the most winners in New Jersey? How was campaign spending by industry changing from cycle to cycle? What industries were behind some of our more notable politicians?</p>

<p style="text-align: center;"><img class="size-full wp-image-56374  aligncenter" src="http://sunlightfoundation.com/media/2013/10/Hackers-at-Hack-Jersey.png" alt="Hackers at Hack Jersey" width="547" height="392" /><br/><em>Hackers at Hack Jersey's Law, Money and Politics Hack day. Photo by Tom Meagher.</em></p>

<p>With that much decided, our team members volunteered to take certain development roles, and we got ready for the hack day. We imagined a front page with a 30,000-foot-view that would show charts of how much industries have spent on all New Jersey campaigns available in the data, going back more than 10 years. After that, we thought our user could drill in to look at specific industries and how their spending changed from cycle to cycle. Or you could put candidates in specific races side-by-side to see what industries supported them.</p>

<p>But we quickly realized that the API, which offers access to individual campaign donations by state, only really returns requests for top industry spending across the whole nation. There was no method (yet) to let us grab the top industries in just a certain state or a specific year.</p>

<p>As the day went on, we hit a few more snags when we realized there wasn't an easy way through the API to get all the candidates who lost elections. So we downloaded the <a href="http://data.influenceexplorer.com/bulk/">bulk data</a> from Influence Explorer and pulled those candidates out ourselves. With each unexpected misstep, the minutes and hours flew by. In the hopes of finishing a project, we'd shrink the scope and tighten our focus.</p>

<p>We finally decided, with a couple of hours left, that we could build a demo app that would let you pick an election cycle in New Jersey, and then browse the available races and see what industries supported each candidate. Two of our developers, who also happen to be the leads for our event sponsor Broadstreet Ads, led the final sprint. They helped pull together a Python web.py framework with Angular.js and Highcharts to power the front end. <a href="http://hackjersey.broadstreetads.com" target="_blank">We could almost see the finish line</a>. And then we ran out of time.</p>

<p>It's hard to build anything in 8 hours, much less bring 15 people together to make a single, deep and useful news application. Although we fell short, we had fun and learned a lot in the process for how to do it better next time:</p>

<ul>
	<li>We could have had a better handle on the very wide range of experience and backgrounds our developers brought to the team. By taking a little more time talking about our skills, we could have focused our project more closely on an attainable goal for such a short window of coding. Time is expensive and in short supply. There is no time for indecision.</li>
	<li>Double the time spent planning before the event, and then double it again. Although we did a good job of considering the overall vision and anticipating some of the quirks of the data, we needed to set very specific tasks for everyone on the team and make sure people were clear about their roles and comfortable. A large group doesn't always lend itself easily to collaborative exploration or problem solving. People need to feel like they're in the mix, especially if they're giving up a Saturday for a civic hack project.</li>
	<li>Do more <a href="http://en.wikipedia.org/wiki/Pair_programming" target="_blank">pair programming</a>. With so many developers, we should have put everyone in pairs from the outset, so each person would have a buddy to help spot mistakes and typos that can eat up precious time. We also could have designated experienced developers as leaders for each aspect (back end, front end, design, documentation), who could have helped make some of the design and implementation decisions more quickly.</li>
	<li>Read the documentation. Test the methods. It seems so simple, but although we spent a few hours with the Influence Explorer documentation, we still kept finding unexpected nuances in the data it returned, very late in the day. If we had spent more time with it, we could have spotted potential detours more quickly.</li>
</ul>

<p>This was an experiment for us. Some experiments don't work, but <a href="http://www.hackjersey.com/2013/09/developing-a-solution-for-tracking-campaign-giving/%20">you can learn a lot from failure</a>. Nearly everyone who participated said they want to work on more news hacking initiatives in the future. Several have said they plan to dig deeper into campaign finance and Sunlight's APIs.</p>

<p>Are you interested in our idea? Take a look at the repo, <a href="https://github.com/hackjersey/politics">fork it and hack away</a>. We'd love to get others involved, whether you're from New Jersey or elsewhere.</p>

<p>Although we didn't get as far as we would have liked, it was a good experience for us at Hack Jersey. We got 15 developers thinking about campaign finance and starting to learn the ins, the outs and the possibilities.</p>

<p>We couldn't grow an orchard in a day, but we planted a lot of good seeds. And that's a pretty good place to start.</p>