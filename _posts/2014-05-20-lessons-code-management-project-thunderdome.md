---
layout: post
title: Lessons in open source code management
Date: 2014-05-20 13:27
Author: Tom
category: blog
Link: /2014/05/lessons-code-management-project-thunderdome.html
Slug: lessons-code-management-project-thunderdome
tags: [Project Thunderdome, version control, coding, newsapps, documentation, open source]
---
<img src="https://source.opennews.org/media/cache/29/6a/296a72f3ab7a102515d96829e0ac138a.jpg" alt="Lessons from the Project Thunderdome Shutdown">
<br />
<br />            
<p><em>Cross-posted from <a href="https://source.opennews.org/en-US/articles/lessons-project-thunderdome-shutdown/" target="_blank">OpenNews's Source</a> blog. This piece ran a few days after the closure of my employer, Digital First Media's Project Thunderdome.</em></p>
<br />
<br /> 
<p>Nearly every time the data team at <a href="http://outsidethunderdome.com/">Project Thunderdome</a> prepared to launch an interactive graphic, a <span class="caps">CAR</span> story, or a news app, I’d say to myself something along the lines of, &#8220;As soon as this hits production, we&#8217;ll go back and beef up the inline documentation to save ourselves headaches the next time we try something like&nbsp;this.”</p>

<p>Of course, despite our best intentions, we never went back until so much time had passed that we’d completely forgotten just about everything we had tried to&nbsp;do. </p>

<p>I suspect that the Thunderdome data team is not peculiar in this respect. But last month, we were given a pretty good reason to revisit our code one last time. Faced with the demise of our newsroom, we decided <a href="https://github.com/thunderdome-data">to open source much of our code</a> under a permissive <span class="caps">MIT</span> license. In doing so, we hope that our now former colleagues at Digital First Media, the nation’s second-largest newspaper company, can fork and reuse our&nbsp;work. </p>

<p>Just as importantly, we hope journalist-developers in other news organizations will build on our code, so they don’t have to reinvent the wheel every time they want to do something simple that we figured out. And maybe, just maybe, sharing this code, as so many other <a href="https://github.com/datadesk">great</a> <a href="https://github.com/texastribune">news</a> <a href="https://github.com/wnyc">organizations</a> <a href="https://github.com/nprapps/">have already done</a>, will encourage more newsrooms to do the&nbsp;same.</p>

<img src="https://pbs.twimg.com/profile_images/2957427857/cca3b69ec0a82cbfb05666f79cf3cd04.jpeg" alt="@DFMdata on Twitter">

<p>On April 2, we learned that <a href="http://www.niemanlab.org/2014/04/the-newsonomics-of-digital-first-medias-thunderdome-implosion-and-coming-sale/">Digital First Media decided to shut down the Thunderdome newsroom</a>. Among our many duties, the data team&#8211;Peggy Bustamante, Vaughn Hagerty, Nelson Hsu, MaryJo Webster, and me&#8211;built interactive news applications and pursued computer-assisted reporting, on our own and with colleagues across the company’s 75 local newsrooms. After the announcement, we were left scrambling to figure out how to finish a half-dozen projects and how to preserve the code behind our work when no one would be responsible for picking up the pieces after we&nbsp;left.</p>

<p>Our team had six weeks to wrap things up, which seemed like plenty of time. But we had projects that we desperately wanted to finish, like our election news game, <a href="http://data.digitalfirstmedia.com/waffler-pa/">The Waffler</a> or our examination of why <a href="http://www.nhregister.com/general-news/20140512/scope-of-nationwide-heroin-epidemic-unknown-drug-related-death-overdose-data-lacking">national data on soaring heroin deaths is so flawed</a>. That left us with a little less than two weeks to clean up our code&nbsp;base.</p>

<p>When I mentioned to <a href="http://www.twitter.com/kleinmatic">Scott Klein</a> that we wanted to prevent nearly two years of work from disappearing, he offered a simple suggestion: open source&nbsp;it. </p>

<p>Last week, as we walked out the door of Thunderdome for the last time, <a href="https://github.com/thunderdome-data">we did just that</a>.</p>

<h3 id="how-we-did-it">How We Did&nbsp;It</h3>
                
        
<p>First, we had to get permission. Our bosses, editor Robyn Tomlin and managing editor Mandy Jenkins, had been incredibly supportive of the data team and our work from the outset, and they didn’t require much convincing. So we had a brief meeting with our <span class="caps">CEO</span>, John Paton, and made our pitch that <a href="http://www.haikudeck.com/open-source-the-dome-inspiration-presentation-lZTwMq34H9">to not publish our code under an open source license would be a waste</a>. To his credit, John, <a href="http://jxpaton.wordpress.com/">who has spoken and written extensively</a> on how our industry needs to innovate and to invest in digital storytelling, required no more convincing. He gave his approval, and we were off and&nbsp;running. </p>

<p>Our next step was to review all of our code that was stuffed into private Github repositories and prioritize projects for release. We put a checklist in a Google Spreadsheet and each member of the team labelled her or his&nbsp;projects:</p>

<ul>
<li>Reusable—we had used this code over and over as a template or that we thought others might find&nbsp;useful.</li>
<li>Just publish—these we’d like to share but were probably discrete and didn’t warrant a lot of additional polishing&nbsp;work.</li>
<li><span class="caps">NO</span>—these were either stories that hadn’t yet published or applications that had a reasonable expectation of being used by our papers for some time, like our crime maps <a href="http://stpaulcrime.twincities.com/">in St. Paul</a> and <a href="http://crime.denverpost.com/">Denver</a>.</li>
<li>Bury it in a swamp—these were so embarrassing or would require such a monumental amount of work to make them presentable, that we preferred to pretend they never&nbsp;happened.</li>
</ul>

<p>We went through scores of repos and categorized them, ending up with about 40 or so that we wanted to release. For each of them, we reviewed all of the code for security and to ensure there was nothing proprietary or worrisome in it. We added a more helpful <span class="caps">README</span> (using a template borrowed from <a href="https://twitter.com/nprviz"><span class="caps">NPR</span> Viz</a>’s <a href="https://github.com/nprapps/app-template">fantastic app-template</a>) and <a href="http://choosealicense.com/licenses/mit/">an <span class="caps">MIT</span> license</a>.</p>

<p>For the most reusable projects, we wanted to offer guidance on how someone else might bootstrap it or abstract the code to make it a more generic template. And this is the area where we simply ran out of time and fell&nbsp;short. </p>

<p>Why? Because as many of you have probably already thought to yourselves, this whole endeavor was inherently flawed. We made this much, much harder on ourselves than it needed to be, because we did it all backwards. We should have been releasing our code as open source from the outset, in a sane way. But when you&#8217;re pushing code on a news deadline and storing it in private repos, robust documentation is not always the priority that it needs to&nbsp;be.</p>

<p>It can be hard to make the case to executives that open sourcing code isn’t the same as giving away the farm. We benefitted in this regard here, because we had a good track record within the company, and we had a body of work to point to. We could honestly say, “Look at this work. There&#8217;s nothing here that would damage the company, and in fact, if we don’t publish this code, we’d be preventing many people in the company from ever using it again.” That this was our dying wish probably helped seal the&nbsp;deal. </p>
        

<h3 id="what-we-ended">What We Ended Up&nbsp;With</h3>
                
        
<p>In <a href="https://github.com/thunderdome-data">our new public Github organization</a> we pushed dozens of projects, built in <span class="caps">HTML</span>, <span class="caps">CSS</span>, <span class="caps">JS</span>, a bit of <span class="caps">PHP</span>, and a smidgeon of Python. Among those, <a href="http://thunderdome-data.github.io">there are nine in particular</a> that we think other newsrooms might find most useful, including a balloting tool, an interactive bracket, a profile tool and more. But we still need help to finish the&nbsp;job. </p>

<p>If you want to use one of these, help us to beef up the documentation and truly abstract it. Fork it and send us pull requests. If you want more advice on how to get started, <a href="http://www.tommeagher.com/about">email me</a>.</p>

<p>And in your own work, start writing good documentation from the start of every project, and don’t wait to open source your code until it’s too&nbsp;late.</p>
        
