# Sobriquet

Hugo theme designed to be utilized as a personal homepage.

## Background

Before writing this theme, I searched long and hard for a theme that would
essentially serve 2 purposes. On the homepage, it would act like a portfolio
page, highlighting things that I've done, but it would also serve deeper content
like blog posts and other miscellaneous tidbits.

Finding nothing that fit this bill to my satisfaction, I created Sobriquet.

The name [Sobriquet](https://en.wikipedia.org/wiki/Sobriquet) came as I was
brainstorming names and found it both distinct and appropriate for this use as
I view my personal website as a kind of virtual nickname for my person.

Please feel free to use and/or fork this theme as your own!

Cheers,  
[Victor Quinn](http://victorquinn.com)

## Configuration

We'll go over each in more detail below, but all of these configurations are
intended to be in your Hugo config file and will be assumed to be under the
params header (so that'll be omitted below).

Here is a full sample config.toml which we'll disect below:

```toml
[params]
    author = "Victor Quinn"
    profile = "VictorQuinn.png"
    segment = "abcd1234"
```

### Personal

Since Sobriquet is intended for use as a Personal website theme, there are some
personal specific configurations that aren't present on most more generic
blog themes.

#### Name

Some personal items include your name, headline, summary, and more. These are
displayed by default on the sidebar.

```toml
    author = "Victor Quinn"
    headline = "Leader of Engineers."
    summary = "Specializing in leading software engineers to build scalable backends."
```

#### Photo

If you're not shy and have a personal photo, it'll be displayed on the sidebar.

Sobriquet expects this image to be placed in the `/static/img/` directory.

```toml
    profile-img = "VictorQuinn.png"
```

#### Social Media

Sobriquet currently supports a bunch of the major social networking platforms.

Simply add the username for each network to your config:

```toml
    facebook = "victorjquinn"
    github = "victorquinn"
    google_plus = "+victorquinn"
    linkedin = "victorquinn"
    reddit = "victorquinn"
    twitter = "victorquinn"
```

If any network is not provided, Sobriquet will automatically hide it.

### Analytics

Sobriquet works with [Segment](https://segment.com) or Google Analytics. I've
long been a huge fan of Segment (which can be used to send data to Google
Analytics as well if you'd like) but also understand that Google Analytics is
often the standard as far as Analytics so that's included as well.

To include it, add the following to your `config.toml`

```toml
# For Segment
[params]
    segment = "your_segment_key"

# or for Google Analytics
[params]
    google_analytics = "your_google_analytics_key"
```
## Creating Content

Sobriquet includes archetypes for the kinds of content that most people may
want on a portfolio site. At current, these include the following:

* Employment
* Education
* Projects
* Writing
* Miscellaneous

If there are others you'd like, feel free to submit a PR, happy to add new
things! I started with items I wanted on my site, but I'm sure there are
likely others, particularly for people in different careers.

Essentially, add content of each archetype, specifying some of the items in the
front matter, and Sobriquet will create a page for that item and add a nicely
stylized card to the front page as well.

For example, to create a new employment item, run the following in your shell

```bash
$ hugo new employment/socialradar.md
```

That'll create a new item using the archetype that will look like this:

```toml
+++
company_img = ""
company_name = ""
company_website = ""
date = "2016-03-06T12:09:47-05:00"
role = ""
summary = ""
time = ""
title = "socialradar"

+++
```

Fill in the front matter items and a nice looking card will be rendered by
Sobriquet on the homepage!

For example, this item ends up looking like this for me:

```toml
+++
company_img = "SocialRadar.png" # Note, this is relative to the /static/img directory
company_name = "SocialRadar"
company_website = "http://socialradar.com"
date = "2016-03-06T12:09:47-05:00"
role = "VP of Engineering"
summary = "Leading the engineering team at a startup focused on location technology."
time = "Sept 2013 - Present"
title = "socialradar"

+++
```

Any content will be put in a new page at /employment/socialradar so you can
fill in further details

## To Do

1. Currently there is no way to re-order the items on the front page. Trying to
figure out a non-confusing way to accomplish this in the config.
