# Jekyll Podcast Feed

This is an example of how to make podcast RSS feeds with Jekyll, including the
information needed to submit it to iTunes.

## Global config

As can be seen in [_config.yml](_config.yml), you need some extra information
to describe your podcast, like this:

    podcast_url: http://www.joebuhlig.com/whaddyaknowjoe
    podcast_album_art: /assets/base/Whaddya-Know-Joe-Album-Art.png
    podcast_title: Whaddya Know Joe?
    podcast_owner: Joe Buhlig
    podcast_email: email@example.com
    podcast_category: Technology
    podcast_subcategory_one: Software How-To
    podcast_subcategory_two: Gadgets
    podcast_explicit: "no"
    podcast_author: Joe Buhlig
    podcast_description: Productivity stories from the trenches...
    podcast_summary: Joe Buhlig walks you through real life story...
    podcast_subtitle: Productivity stories from the trenches...

## Individual posts

Posts (e.g. [_posts/2017-02-08-my-first-podcast.markdown](_posts/2017-02-08-my-first-podcast.markdown))
need some extra config at the top too:

    categories: podcast
    podcast_link: http://traffic.libsyn.com/podcast/filename.mp3
    podcast_file_size: 13.7 MB
    podcast_duration: "14:02"
    podcast_length: 13654375

If you include this code in a post:

    {% include audio.html %}

An audio player will appear in the blog post.

## Multiple feeds

The default setup is to generate two feeds - one for Ogg Vorbis and one for
MP3.  If you want to remove one, simple delete e.g.
[podcast-mp3.xml](podcast-mp3.xml).

To add other file types, copy [podcast-mp3.xml](podcast-mp3.xml) and modify it
to specify the correct file extension.

## Testing locally

If you have Jekyll set up as usual, this should work:

    git clone git@github.com:andybalaam/Jekyll-Podcast-Feed.git
    cd Jekyll-Podcast-Feed
    jekyll serve

Now you should be able to see the example site at
http://127.0.0.1:4000/Jekyll-Podcast-Feed/ and the example podcast feeds at
http://127.0.0.1:4000/Jekyll-Podcast-Feed/podcast-ogg.xml and
http://127.0.0.1:4000/Jekyll-Podcast-Feed/podcast-mp3.xml

## podcast_guid

You can also provide `podcast_guid` for a post to preserve permalinks from a
previous site:

    podcast_guid: ?p=866

## Examples

* http://joebuhlig.com/whaddyaknowjoe/
    * http://joebuhlig.com/feed/podcast
* http://www.artificialworlds.net/imagine/
    * http://www.artificialworlds.net/imagine/podcast-ogg.xml
    * http://www.artificialworlds.net/imagine/podcast-mp3.xml
