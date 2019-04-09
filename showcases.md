---
layout: page
title: Showcases
permalink: /showcases/
---
There are tens of thousands of developers and designers who use Fuse to build awesome cross-platform native apps. Here's a small selection of apps made with Fuse. 
Want to be featured? [Let us know!](mailto:fuse-open@googlegroups.com)

<div class="showcases row">
  {% for showcase in site.showcases %}
  <div class="col-12 col-sm-6 col-md-4 col-lg-3">
    <div>
      <h2><a href="{{ showcase.url }}">{{ showcase.title }}</a></h2>
      <a href="{{ showcase.url }}">
        <img class="mw-100" src="{{ site.baseurl }}/assets/images/{{ showcase.id }}.png" alt="{{ showcase.title }}" />
      </a>
      <p>{{ showcase.synopsis }}<br><a href="{{ showcase.url }}">Read more</a></p>
    </div>
  </div>
  {% endfor %}
</div>
