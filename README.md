## Creating a post

The file structure is as follows:

``` text
content
  post
    year
      month
        day-title.md
```

Here's an example post:

    ---
    title: "Episode 14: The Unoffended"
    date: 2018-12-20
    youtubeid: "GZKxkuktzQo"
    ---

    * [We, The Unoffended](http://blog.cleancoder.com/uncle-bob/2018/12/16/unoffended.html)
    * [Agile Manifesto](https://agilemanifesto.org/)
    * [Space Hack](https://www.facebook.com/spaceappskl/)
    <!--more-->
    * [REconference](https://www.eventbrite.com/e/conference-2018-october-2018-tickets-50674235001) - sold out
    * [Cytron](https://www.cytron.io/)
    * [Fractals: L System](https://en.wikipedia.org/wiki/L-system)
    * [g0v](https://summit.g0v.tw/2018/ https://g0v.tw/en-US/)
    * [Hack/Hackers kl](https://www.facebook.com/HacksHackersKL/)

The front matter contains three attributes:
* **title** - the title of the post. This also determines the filename, so it's best not to use special characters like `#`
* **date** - the date of the post. This also determines the chronological order of the posts in the index
* **youtubeid** - the youtube id of the live recording. The blog will automatically create the youtube embed for you

Below the frontmatter are the shownotes. We want to display a maximum of four on the index page. If there are more than four (i.e. five or more) we get the top three and put the comment `<!--more-->` and then the rest of the show notes. This creates a `[read more]` link on the index page
