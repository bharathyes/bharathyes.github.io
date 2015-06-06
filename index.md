---
layout: page
tagline: "Awesome Coder, film fanatic, proud Macintosh owner."
tags : [Home]
---


<ul class="post-list">
{% for post in site.posts %}
<li>
<span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>

<a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
<h2 class="post-title" style="color:#E16400;">
{{ post.title }}
</h2>
{% if post.description %}
<h4>{{ post.description | strip_html }}</h4>
{% else %}
<h4>{{ post.excerpt | strip_html }}</h4>
{% endif %}
{% if post.image %}
<img src="{{ post.image }}" alt="" max-height="500px"/>
{% endif %}<hr>
</a>
</li>
{% endfor %}
</ul>


