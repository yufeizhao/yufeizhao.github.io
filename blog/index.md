---
layout: default
title: Yufei Zhao | MIT Mathematics
description: "Assistant Professor of Mathematics at MIT. Research area: combinatorics"
---

<h1 class="content-listing-header sans">Blog</h1>

[List of entries](list)

<ul class="content-listing ">
  {% for post in site.posts %}
      <li class="listing">
        <a href="{{ post.url | prepend: site.baseurl }}"><h2>{{ post.title }}</h2></a>
        <span class="smaller">{{ post.date | date: "%B %-d, %Y" }}</span>  <br/>
        <div>{{ post.excerpt }}</div>
        <hr class="slender">
      </li>
  {% endfor %}
</ul>

