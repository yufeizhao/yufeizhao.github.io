---
layout: default
title: Yufei Zhao | MIT Mathematics
description: "Assistant Professor of Mathematics at MIT. Research area: combinatorics"
---
<div class="blog">

<h1 class="content-listing-header sans">Blog</h1>

<p>
<a href="/blog/">Back to main</a>
|
{% include rss_logo %}
</p>

<ul>
  {% for post in site.posts %}
      <li >
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        <span class="smaller">{{ post.date | date: "%-m/%-d/%Y" }}</span>  
        <br/>
      </li>
  {% endfor %}
</ul>

</div>