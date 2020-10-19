---
layout: page
title: Blog posts
meta_description: "Blog posts - filfreire.com"
permalink: /posts/
---

<section>
    <p><strong>Disclosure</strong> - views expressed in this blog are mine and do not reflect the views of my employer, or any organization I am affiliated with.</p>
</section>

<ul>
    {% for post in site.posts %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>,
        <small><span>{{ post.date | date:"%B %d, %Y" }}</span></small>
    </li>
    {% endfor %}
</ul>

