---
layout: default
title: Yufei Zhao | Blog
description: "Blog of Yufei Zhao, Assistant Professor of Mathematics at MIT"
---


<div class="blog">
<h1 class="content-listing-header sans">Blog</h1>

<p>
<a href="/blog/list/">List of entries</a>
|
{% include rss_logo %}
</p>

{% for post in site.posts %}
{% unless post.draft %}
<h2><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
<p><span class="smaller">{{ post.date | date: "%B %-d, %Y" }}</span></p>
<div>{{ post.excerpt }}</div>
<hr class="slender"> 
<br/>
{% endunless %}
{% endfor %}

</div>