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

```toml
    name = "Victor Quinn"
```

#### Photo

If you're not shy and have a personal photo, it'll be displayed on the sidebar.

Sobriquet expects this image to be placed in the `/static/img/` directory.

```toml
    profile-img = "VictorQuinn.png"
```

#### Social Media

Sobriquet currently supports a bunch of the major social networking platforms.

Simply add the username for each network to your confi:

```toml
    facebook = "victorjquinn"
    github = "victorquinn"
    google_plus = "+victorquinn"
    linkedin = "victorquinn"
    reddit = "victorquinn"
    twitter = "victorquinn"
```

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
