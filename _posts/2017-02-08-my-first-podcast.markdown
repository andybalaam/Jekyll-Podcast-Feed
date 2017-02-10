---
layout: post
title:  "My First Podcast"
date:   2017-02-08 02:07:00 +0000
categories: podcast
podcast_link: /audio/free-software-song
podcast_duration: 01:48"
podcast_length: {"ogg": 326823, "mp3": 108621}
---
This post is in the podcast category so it will be included in your podcast RSS
feeds.  (You can see the feed subscribe links at the bottom of the page.)

It also includes an audio tag so people visiting the blog can play it directly:

{% include audio.html %}

Your podcast posts must contain metadata like this:

    podcast_link: /audio/my-first-podcast
    podcast_duration: "32:04"
    podcast_length: {"ogg": 29870091, "mp3": 30785454}

Notice that there is no file extension on the link - it will be added based
on the type of feed (ogg or mp3).

Put your audio files inside the `audio/` directory and add their details to the
podcast metadata.
