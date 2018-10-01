---
title: Meetups
subtitle: Pickled and Curated with Love by Actual Human Beings
comments: false
layout: "meetups"
---

Want your meetup added? Send a [PR](https://github.com/DevxKami/devkami.com/blob/master/data/meetups.yml) and we'll get it merged for you! :)

<script>
var content = document.getElementsByClassName("blog-post")[0];
var links = content.getElementsByTagName("a");

for (var i = 0, linksLength = links.length; i < linksLength; i++) {
   if (links[i].hostname != window.location.hostname) {
      links[i].target = '_blank';
   }
}
</script>

<form method="POST" action="{{ .Site.Params.staticman_api }}">
  <input name="options[redirect]" type="hidden" value="{{ .Permalink }}#post-submitted">
  <input name="options[redirectError]" type="hidden" value="{{ .Permalink }}#post-error">
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <label><input name="fields[name]" type="text">Name</label>
  <label><input name="fields[email]" type="email">E-mail</label>
  <label><textarea name="fields[message]"></textarea>Message</label>

  <button type="submit">Go!</button>
</form>
