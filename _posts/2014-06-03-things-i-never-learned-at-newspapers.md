---
layout: post
title: Things I never learned at newspapers about making news on the internet
Date: 2014-05-20 13:27
Author: Tom
category: blog
Link: /2014/06/things-i-never-learned-at-newspapers.html
Slug: things-i-never-learned-at-newspapers
tags: [Project Thunderdome, design, coding, newsapps]
---
_Adapted from a lightning talk I gave at ASNE's [Hacking News Leadership](http://asne.org/blog_home.asp?Display=1695) conference in Austin, Texas in May. You can see my original slides here: [http://bit.ly/tdnewslead](https://www.haikudeck.com/lessons-from-thunderdome-art-and-design-presentation-CHZ3Wu9ZR4)._
<br />
<br />
<img src="/images/tdome.png">
<br />
<br />
Over 21 months at Thunderdome, we created a lot of great projects, from interactive graphics for the [Newtown shootings](http://extras.twincities.com/elections/sandyhook/) and the [Boston marathon bombings](http://www.sentinelandenterprise.com/webextras/ci_23055737/interactive-people-boylston-street-during-boston-marathon-bombing) to [deep-dive data analyses](http://www.sltrib.com/sltrib/news/56473395-78/claims-veterans-lake-salt.html.csp?page=1) and [visualizations](http://www.twincities.com/nation/ci_25247140/where-insurance-premiums-are-highest-new-health-laws). They included pieces like:

* [Our crime map](http://crime.denverpost.com/) framework
* [The Waffler](http://data.digitalfirstmedia.com/waffler-pa) news game
* [Firearms in the Family](http://data.digitalfirstmedia.com/guns/)

With each of these projects, [our data team](http://thunderdome-data.github.io) and [our colleagues across the newsroom](http://outsidethunderdome.com/2014/04/30/project-thunderdome-staff/index.html) learned so much. We learned new ways to visualize data and new code libraries for user interaction. We learned about code management and [how to (and how not to) open source](http://www.tommeagher.com/blog/2014/05/lessons-code-management-project-thunderdome.html) our work. We learned how to report, design and release smarter, more engaging interactives. As we wrapped things up in our closing days, I realized that some of the biggest lessons from our time at Thunderdome were more cultural than technical, and they were ones we never anticipated in our previous jobs in print-first newsrooms.
<br />
<br />

<img src="/images/deli.png">

##The Internet is not a deli

The first misconception newspaper veterans have is the notion that interactive news teams are simply new-fangled print graphics desks. Although the two roles have skills in common (visual-thinking, smart data presentation), there are enough differences to make the comparison worrisome. Many newsrooms treat their graphics desk like a deli counter. A reporter reports a story and files it on deadline. At that point, an editor looks at it and says, "We should have a graphic for this." That editor takes a number from the graphics desk, if there is one, and waits for a suitable print-ready image to be sliced to size.

This mindset, and the idea that interactive news developers should be a support desk, is counter-productive (pardon the pun). This work is too expensive, in terms of time and resources, to follow the old print graphics desk model. Journalist-developers must be woven into the assigning side of the newsroom and involved in stories from the very beginning, not sitting around waiting to pretty things up at the last minute. At ProPublica, the developers on Scott Klein's news apps team are expected to not only design and build interactives for the web, but also to help with the reporting. They're involved in the entire process, from start to finish.

This is a hard adjustment for newspaper reporters, who are accustomed to having time to figure out what their story is before filing it at the last possible minute. They need to think on a timeline that allows developers to help. We can build on deadline when news demands, but the rest of the time, we shouldn't have to.

It took a while for the data team to figure out how to deal with this. We noticed a turning point when we stopped waiting for other desks to pitch ideas on our timetable and began to pursue more of our own projects. Anyone was welcome to join the fun, but we knew if we wanted to get something good done for the 50th anniversary of JFK's assassination in November, for instance, we'd need to start working on it in August. [And it worked](http://data.digitalfirstmedia.com/jfk/).
<br />
<br />

<img src="/images/team.png">

##Hire new skills

When we started Thunderdome, there were several roles we weren't even thinking about that became integral to our online storytelling.

In the original plan for the newsroom, there was no data team. Thankfully, our editor, Robyn Tomlin, knew we needed one.

We also didn't initially think about web design, front-end programming or motion graphics. These were jobs we never had at any of the newspapers I worked at. But without the first two, our data team couldn't have done a single interactive project. Without our awesome motion graphics designer, our presentations for many of our later projects would have been lackluster, at best.

The expertise that this new style of storytelling demands simply doesn't exist in most news organizations. Our job is to develop these skills where we can and to hire for them now, and the smart editors will recognize that you're probably not going to find people with these skills by only posting on journalismjobs.com.
<br />

##Herd all the cats

In a newspaper, the chain of command, established over a century of practice, is very simple and well-known. In our interactive newsroom, it was a little harder to determine sometimes.

For many of our more ambitious stories, we had contributors from the data team, the design team, the video team and the features, news and sports desks. We'd often be working with reporters or editors at the local DFM papers. Many of our most successful projects crossed traditional department boundaries. But we noticed quickly that it wasn't which editor should be orchestrating the work.

In one case, we had a really outstanding intern coordinating a project, but there was confusion between myself and another editor as to which of us was really in charge. We learned that projects like these require new levels of collaboration, and that’s not always easy. You need someone who can corral the players across the newsroom, as well as someone in a traditional editor’s role, focused on getting the story right and telling it well. We started to insist that every project have a project manager and an editor, someone calling the shots.

Anyone *can* lead a project, but somebody *must* lead.
<br />
<br />
<img src="/images/break_the_cms.png">

##You need a sandbox

An interactive team must have a space outside of the CMS to experiment and to be able to break shit without bringing down the entire system. At one point at Thunderdome, the local papers in our company had at least four CMSes. Trying to build interactives that would painlessly work in each system was a monstrous task. But without a sandbox of our own to experiment in, it would have been impossible.

Most CMSes are designed to prevent the kind of monkeying around that this new kind of online storytelling requires. News development teams that do this well all run their own servers, often in the cloud through something like [Amazon Web Services](http://aws.amazon.com/). This give the flexibility to try new tools and to iterate at a speed that most corporate IT departments just can't adapt to. If you're starting a team from scratch, the very first thing you have to do is [give it the tools it needs to succeed](http://thescoop.org/archives/2014/05/22/how-it-starts/), and an autonomous development sandbox is at the top of that list.
<br />

##Iteration leads to bigger successes

Failure is an option. Our data team was willing to try anything new, knowing that even if it bombed spectacularly, we'd walk away with the know-how to make our next project work.

Many of our most successful apps began as more humble ones. We iterated and used most of what we learned from [the JFK project](http://data.digitalfirstmedia.com/jfk/) on the [Firearms in the Family](http://data.digitalfirstmedia.com/guns/). [Bracket Advisor](http://www.bracketadvisor.com/) was the second or third iteration of a tool we originally created with our sports desk for [the NFL playoffs](http://www.twincities.com/1000/ci_22346309/predict-nfl-playoffs?mobRedir=false).

At a daily newspaper, looking back at how well a story succeeded was never even considered. To be fair, when you're writing quick stories every day, you learn and adapt much faster. When your projects take weeks, or sometimes months, that learning process has to be more deliberate.

The key to good iteration was in our post-mortem reviews. After each deployment, we'd pause to collect our thoughts, to write down what worked and what didn't and to craft a list of features we'd want in the next project. Then we'd use those ideas over and over again to make our work better.<br />
<br />
<img src="/images/culture_is_contagious.png">

##Be the journalist you want others to become

If you do good work, other journalists will pay attention. Every project was a learning opportunity for our team, for colleagues at Thunderdome and at our local papers.

A big part of our data team's mission was to evangelize for smart watchdog reporting, strong data analysis and good online presentation. We wanted to share our ideas and to learn from our colleagues. It was gratifying to see others pick up on this, whether it was a producer in Thunderdome embracing [DocumentCloud](http://www.documentcloud.org/home) or an editor in Michigan asking for advice on tools for searchable tables and interactive maps.

When we began, we inherited a small email list of a couple dozen local DFM journalists who were data-curious. By the time Thunderdome shut down, the listserv had grown to about 120 people, from San Jose to New Haven. Newspaper journalists want to learn how to do data analysis and develop for the web. A newsroom that supports them in practicing and mastering those skills will reap the benefits. You have to start building that culture.
<br />

<br />
<br />

_All images are Creative Commons-licensed. You can see the credits for each of them here: [http://bit.ly/tdnewslead](https://www.haikudeck.com/lessons-from-thunderdome-art-and-design-presentation-CHZ3Wu9ZR4)_.