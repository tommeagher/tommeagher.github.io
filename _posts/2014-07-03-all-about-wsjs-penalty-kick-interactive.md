---
layout: post
title: All about the WSJ's penalty kicks interactive
Date: 2014-07-03 13:27
Author: Tom
category: blog
Link: /2014/06/all-about-wsjs-penalty-kick-interactive.html
Slug: all-about-wsjs-penalty-kick-interactive
tags: [newsapps, data, soccer, worldcup]
---

_Cross-posted from [Open News' Source blog](https://source.opennews.org/en-US/articles/all-about-wsjs-penalty-kick-interactive/)._

<p><em>In the days before the World Cup&#8217;s knockout stages, with their potential for games to end in shootout finishes, The Wall Street Journal unveiled an app that visualized the tendencies of the top <a href="http://graphics.wsj.com/wc-penalty-kicks/">penalty kicks takers</a> on the teams advancing in the tournament. <a href="https://twitter.com/ccanipe">Chris Canipe</a>, senior news apps developer on the Wall Street Journal&#8217;s interactive graphics desk, talked with me about the thinking behind the project and how he and his colleagues put it together. What follows are edited excerpts from our&nbsp;conversation.</em></p>

        <h3 id="concept">The&nbsp;Concept</h3>

        <p>The World Cup [interactive coverage] working so well has been completely a product of working with great reporters, who knew what they wanted to do and had great ideas. That makes all the difference. Geoff Foster is one of our main sports guys, and Matthew Futterman, <a href="http://online.wsj.com/articles/with-his-eye-on-the-world-cup-soccer-coach-jurgen-klinsmann-overhauls-team-usa-1401899734">who wrote the Klinsmann profile</a>, wanted to focus on penalty kicks. Geoff Foster had done <a href="http://online.wsj.com/article/6BE4CA76-48F1-4519-8A12-8E5683D8CAAD.html#!6BE4CA76-48F1-4519-8A12-8E5683D8CAAD">a video about saving penalty kicks</a> where he went to the Red Bulls&#8217; practice facility and talked to a goalkeeper about&nbsp;them.</p>

<p>Penalty kick success rates are very high. It&#8217;s almost paper, rock, scissors. You go right, you go left or you go middle.
But very rarely people go middle. (Freakonomics <a href="http://freakonomics.com/2010/06/14/what-to-do-with-your-penalty-kick/">looked at this phenomenon</a> in the runup to the World Cup in South Africa, four years&nbsp;ago.)</p>

            <img src="https://source.opennews.org/media/img/uploads/article_images/pk2.png" alt="Penalty kicks">

<p>Overall success rates are about 78 percent. If you kick to the middle, that goes up 7 percent, because a goalie, they are diving to the left or diving to the right&#8211;they don&#8217;t have time to think about&nbsp;it.</p>

<p>I&#8217;m a baseball guy. [This penalty kick analysis is similar to] the idea of where to place fielders based on a hitter&#8217;s spray&nbsp;pattern.</p>

        <h3 id="data">The&nbsp;Data</h3>

        <p>We have a pretty good data provider we work with called <a href="http://www.optasports.com/">Opta</a>. They&#8217;re particularly good with soccer data. They gave us all kinds of stuff. Included in the game event summaries, they had X- Y- and Z- coordinates for penalty kicks. We were really impressed with the level of&nbsp;detail.</p>

<p>It was really easy to put in a request, &#8220;Here&#8217;s a list of players, can we get every penalty kick that they&#8217;ve ever&nbsp;taken?&#8221;</p>

<p>There were some limitations with the data set. Not everybody has a significant body of penalty kicks in their career. (Opta also doesn&#8217;t have comprehensive data for players on club teams outside the highest echelons, making it harder to get stats for someone who plays in the Iranian league, for&nbsp;instance).</p>

<p>We kind of wanted to do this at the beginning [of the tournament], but the more we played with the data, the more we sketched it out, we saw it would work better with a smaller number of&nbsp;teams.</p>

<p>[We settled on] two players for each team in the round of 16, but still we have a bunch of the guys in the set who only have one kick. Algeria, we only had one player [with data]. We were hoping for Russia to beat Algeria (to advance out of the group stage) because we had two guys for&nbsp;Russia.</p>

<p>This doesn&#8217;t comes as <span class="caps">XML</span> or <span class="caps">JSON</span>; this comes as a spreadsheet. You get the matchup, the date&#8230; X is length of the pitch, Y is the length of the goal side of the field, Z is up and down. [For a goal, you get the] end-Y and end-Z position, and end result or outcome. It&#8217;s either a goal, or it&#8217;s saved, or it hit the posts or it&#8217;s a&nbsp;miss.</p>

            <img src="https://source.opennews.org/media/img/uploads/article_images/gameday.jpg" alt="pitch-by-pitch">


<p>As a baseball fan, I think of <a href="http://mlb.mlb.com/mlb/gameday/index.jsp?gid=2014_07_02_phimlb_miamlb_1#gid=2014_07_02_colmlb_wasmlb_1&amp;mode=gameday"><span class="caps">MLB</span>&#8217;s pitch-by-pitch Gameday view</a>.
I always figured that part of [the data collection] was some computer recording the position. But it&#8217;s these data vendors [like Opta]. They employ rooms full of people who are watching every event of the game and coding it. That&#8217;s really&nbsp;interesting.</p>

<p>We ran into an issue initially where we had Y-positions that were reversed on the field, because Opta had not corrected&#8211;we caught it&#8211;which side of the field kicks were being taken&nbsp;from.</p>

<p>To catch problems in the data, you go and watch lots of videos and make sure everything is lining up. You find as many of these on YouTube as you can, so you have confidence all of them are&nbsp;correct.</p>

<p>When we got the [corrected] data back [from Opta], we watched maybe 10 kicks, random spot checks. It&#8217;s hard to find video of these. You have a shaky cell phone view of people watching on&nbsp;<span class="caps">TV</span>.</p>

<p>You&#8217;re working with data that is hand-coded, so any time you&#8217;re working with a vendor like this, you&#8217;re taking a little bit of a risk. There&#8217;s a lot of room for human error in something like&nbsp;this.</p>


        <h3 id="design">Design</h3>

        <p>The actual work itself, it was not hard to put together. The hard part was narrowing down and coming up with what we wanted to say with&nbsp;it.</p>

<p>It worked really well as a small multiples piece, because you get to compare all of these guys together, especially if they have a large enough sample size, like <a href="http://graphics.wsj.com/wc-penalty-kicks/#/?sel=19054">Messi</a>, <a href="http://graphics.wsj.com/wc-penalty-kicks/#/?sel=53645">Hulk</a>, <a href="http://graphics.wsj.com/wc-penalty-kicks/#/?sel=40720">Cavani</a>.</p>

<p>It&#8217;s built with D3. The <a href="http://www.propublica.org/nerds/item/design-principles-for-news-apps-graphics">small multiples</a> approach was sort of obvious from the beginning. Part of the reasoning is that it reflows so easily for mobile. Small multiples&nbsp;rule.</p>

<p>You want to see guys side-by-side. Do guys spread out their kicks? How many guys actually do go to the middle? Most guys go left or&nbsp;right.</p>

            <img src="https://source.opennews.org/media/img/uploads/article_images/pk1.png" alt="PKs">


<p>There&#8217;s that filter in the top, &#8220;Trends Left&#8221; or &#8220;Trends Right.&#8221; Nobody trends to the middle, except for the guys who had two kicks in their&nbsp;set.</p>

<p>After launch, <a href="http://graphics.wsj.com/wc-game-recaps/#/?g=731815">that first game</a>, was a shootout. It almost made us seem prescient. I was sitting at home, watching that game. The Journal main desk tweeted it out. We got a ton of traffic right at that moment. In that first game, you could see penalty kick patterns for <a href="http://graphics.wsj.com/wc-penalty-kicks/#/?sel=42565">Vidal</a> and&nbsp;Hulk.</p>

<p>This is definitely not a case where it goes up, and the traffic dies off immediately. All of our stuff, I&#8217;m really surprised how much social traffic things are&nbsp;getting.</p>

<p>This is the beauty of the World Cup stuff. It has this sort of long&nbsp;life.</p>

<img src="http://graphics.wsj.com/wc-penalty-kicks/images/goal.png" alt="An open net" />
