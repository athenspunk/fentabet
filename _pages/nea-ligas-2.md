---
ID: 2654
post_title: Νέα Σούπερ Λίγκας
author: cbr
post_excerpt: ""
layout: page
permalink: http://www.fentabet.eu/nea-ligas-2/
published: true
post_date: 2016-09-19 22:38:00
---
[insert_php]


$feed = file_get_contents('http://www.novasports.gr/sys/novasports/RssFeed/GetFeed?type=1&id=13&languageID=1');
$feed = str_replace('<media:', '<', $feed);
$rss = simplexml_load_string($feed);
$rss = simplexml_load_file('http://www.novasports.gr/sys/novasports/RssFeed/GetFeed?type=1&id=13&languageID=1');

foreach ($rss->channel->item as $item) {
    
   echo '<h2><a href="'. $item->link2 .'">' . $item->title . "</a></h2>";
   echo "<p>" . $item->$media. "</p>";
   echo "<p>" . $item->description . "</p>";

}

[/insert_php]