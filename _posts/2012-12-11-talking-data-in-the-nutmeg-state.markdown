---
author: Tom
comments: true
date: 2012-12-11 17:08:02+00:00
layout: post
slug: talking-data-in-the-nutmeg-state
title: Talking data in the Nutmeg State
wordpress_id: 1187
category: blog
tags: [data journalism, Fusion Tables]
---

_Update: In mid-December, I led two days of training in data journalism techniques for my colleagues at the New Haven Register. On a Thursday evening, I took the Amtrak train home to New Jersey, feeling good about turning a group of journalists on to the power and fun of incorporating data into their reporting._

_The next morning, the horrible shooting at Newtown Elementary School threw our world upside-down. Only now, more than two months later, have I been able to take a moment to revisit the rough notes and links I dumped here in December to try to make them a little more useful._

_The first class was an overview discussion of "data journalism" and the many and sundry techniques that encompasses. The second class was a hands-on walk-through of Excel and Google Fusion Tables. The handouts and cheatsheets cover nearly all of the tips we discussed. If you have questions, or would like to know more, please leave a comment or send me an email._


## Intro to data -[ slide deck](http://www.haikudeck.com/p/sd9NVKceJ0)

### Handouts:
	
  * [Newsroom math overview](/files/tips/mathhandout.doc)	
  * [Numbers in the Newsroom by Sarah Cohen](/files/tips/NumbersintheNewsroom.doc) by Sarah Cohen
  * [Newsroom math crib sheet by Steve Doig](/files/tips/NewsroomMathCribSheet.doc)

### Extra reading
	
  * [The roots of "precision journalism"](http://www.sampler.isr.umich.edu/2011/featured/revealing-the-roots-of-a-riot/  )	
  * [How Jason Hoppin predicted a close local election](http://www.santacruzlive.com/blogs/online/2012/11/27/how-sentinel-reporter-jason-hoppin-predicted-the-outcome-of-local-supervisors-race/  )	
  * A video of [Ben Welsh](http://www.palewire.com)'s [talk on data journalism](http://youtu.be/iP-On8PzEy8). He explains it very well, "It's only in journalism that we continue to distinguish ourselves with the use of Microsoft Excel."

* * *


Hands-on Excel & Fusion Tables class

Data for Excel exercises

  * [Schoolsdatav1.xlsx](http://blog.tommeagher.com/wp-content/uploads/2012/11/schoolsdatav1.xlsx)	
  * [2010-2011hs-prresults.xlsx](http://blog.tommeagher.com/wp-content/uploads/2012/11/2010-2011hs-prresults.xlsx)
  * [DemographicSnapshotEdited.xlsx](http://blog.tommeagher.com/wp-content/uploads/2012/11/demographicsnapshot2012public.xlsx)
  * [Appointments.xls](http://blog.tommeagher.com/wp-content/uploads/2008/09/3appointmentsclass.xls)
  * [Crony.xls](http://blog.tommeagher.com/wp-content/uploads/2008/09/8crony.xls)
  * [citybud.xls](http://blog.tommeagher.com/wp-content/uploads/2008/09/10citybud.xls)

Let’s do something fun and map the data for a story, using Google's experimental (and free) [Fusion Tables](http://tables.googlelabs.com/) program. We're going to download a spreadsheet in the CSV format of the violent crime rates for every town in Connecticut.

Go to [DataHaven.org](http://www.datahaven.org) Go to indicators>Public safety>Community safety>Violent crimes> total violent crime rate
Select all towns and hit the submit button. Click "All years" and hit submit again. Now you can download the CSV, which stands for comma-separated values. It's essentially a spreadsheet without any of the fancy highlighting or formatting of Excel. It's a universal format, and when given the option, it's a good idea to get your data in CSV. Because of its simple structure, it's easy for a human to read and just about any computer can understand it.

Now, we have our data, but if we want to visualize it, we need a map to put it on. We can get this map from a SHP (pronounced "shape") file.  Luckily, in many states, the government or academic institutions often have a clearing house for this kind of geographic data. In Connecticut, you can find it at the U. Conn. library. Point your browser toward [http://magic.lib.uconn.edu/](http://magic.lib.uconn.edu/), then look under the "CT GIS" column and click on the "[Boundaries](http://magic.lib.uconn.edu/connecticut_data.html#boundaries)" section.

Grab the "Connecticut Towns" shapefile from 2010. Then you have to convert the file to a format that Fusion Tables can use. Luckily, there is a free website called "[Shp Escape](http://shpescape.com/)" that can help. Give it your shp file and log into your Google account and it will automatically transform the file and ship it into your Fusion Tables account. Some times the site can be a little busy, so it may take a few minutes. Be patient.

Now, that you have your map file in Fusion Tables, you need the data you want to visualize. Go to Google Drive, click the "create" button and choose Fusion Table. Choose the "download.csv" file that you got from Data Haven and put this into your Fusion Table. (Notice, Fusion Tables also allows you to import tabular data directly from a Google Spreadsheeet.

Clean up the column headings in the file to make the more meaningful. Now we're going to merge the data file back to the shape file we already uploaded. Under the "File" dropdown menu, choose "Merge." Find your Connecticut Towns shape table. And you have to determine which field to join the tables on. What field is the same in both tables? Notice that the "town" field in the crime table matches the "NAME10" field in the shape file. That's your key to join the tables together. Just be certain that each town name only appears once in that column in each table (in this example, it does).

Once it sends you into Fusion Tables, click the "About this table" link under the File dropdown menu and "edit table information." Update the name of the table, give it a meaningful description, attribution and a link to the original download. This can help you later to retrace your steps and bulletproof your reporting. It will also help others who look at your work and want to see your primary source material. Click on the "Share" button and make the map public.

We have both tables combined together into one, new, merged table. But if you click on the "Map" tab, it probably still doesn't look right. We need to style the representation of the data. While you're on the map tab, go to the "Tools" dropdown and click on "Change Map Styles." This will allow us to choose how we want to color code the towns based on their crime rate. Instead of points, we want to click on "Fill color" under the "Polygons" section. Points would be if we were color-coding pins on individual addresses. Instead, we want to shade an entire town based on its crime rate, thus we want "polygon." For the fill color, let's pick the "buckets" tab, which means we can choose four different colors to represent the range of crime rates in our area. If you want to fancy, you can choose whatever color you want for each bucket. Hit the "save" button. Are all of your towns filled in with a color? (You can ignore the "[Southwick Jog](http://www.cslib.org/jog.htm)"). If not, then you probably haven't set the range of values for your crime rate to the include all of them. Adjust the high and low ends of your range until none of your towns are blank. This may take some jiggering.

Play with the bucket sizes and colors of the buckets. What makes sense? Is everything in there?

Click on the title to change the attribution and background info for the merged table. Share the merged table and make it public. Then click Tools> Publish. This gives you the embed code for you to put it in your story.

Once you get the hang of this, you can but producing web-ready interactive maps in 20-30 minutes, a task that would have taken hours or days not all that long ago. This is an awesome tool.



There are a few more things that you can tweak, if you like. You can go to Tools>Change info window layout, to tweak the information that's displayed when you click on a polygon.

And one last tip, you don't always have to upload your own data or map files. You can go to Help>Search Public Tables and browse through all of the data that other Fusion Tables users have uploaded. Of course, as with all reporting, the caveat is to mindful of the source. Always confirm the information and data with other parties. But if you find a good shapefile, you could use it again and again. It's definitely worth exploring.

That's the super fast and dirty introduction to Fusion Tables. Now, go explore it some more on your own. What's your favorite trick in Fusion Tables? Drop me an email, leave a comment or mention me on Twitter and I'll add it here.

Tipsheets and tutorials

  * [Getting around Excel](/files/tips/xlgetaround.doc)
  * [Sorting in Excel](/files/tips/xlsort.doc)
  * [Power formulas in Excel](/files/tips/xlpowerformula.doc)
  * [Excel filters and pivot tables](http://businessjournalism.org/wp-content/uploads/2012/03/xlpivot_updated.pdf)
  * [More Fusion Tables tutorials](http://support.google.com/fusiontables/answer/184641/?hl=en&)
  * [Examples of cool uses of Fusion Tables](https://sites.google.com/site/fusiontablestalks/stories)