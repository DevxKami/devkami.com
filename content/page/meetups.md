---
title: Meetups
subtitle: Come and connect with fellow developers!
comments: false
type: "page"
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
