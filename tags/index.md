---
layout: page
current: tags
title: Tags
navigation: true
logo: 'assets/images/ghost.png'
class: page-template
subclass: 'post page'
---

<p style="text-align: center; line-height: 3em;">
{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign tags = site_tags | split:',' | sort: 'title' %}
{% include tagcloud.html %}
</p>
