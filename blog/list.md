---
layout: default
title: Yufei Zhao | Blog
description: "Blog of Yufei Zhao, Associate Professor of Mathematics at MIT"
image: /photo.jpg
---
<div class="blog">

<h1 class="content-listing-header sans">Blog</h1>

<p>
<a href="/blog/">Back to main</a>
|
{% include rss_logo %}
</p>

<ul>
  {% for post in site.posts %} {% unless post.draft %}
      <li>
        {% if post.image %}<img class="side" src="{{ post.image }}" style="max-height:4rem">{% endif %}
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        <span class="smaller">{{ post.date | date: "%-m/%-d/%Y" }}
        <br/>
        {{ post.description }}
        </span> 
      </li>
  {% endunless %}{% endfor %}
</ul>

</div>