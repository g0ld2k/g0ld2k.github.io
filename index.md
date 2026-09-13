---
layout: default
description: Independent Apple apps by Chris. Explore Zoner, Contadino, and Distance Track.
---

<section class="home-intro" aria-labelledby="intro-title">
  <h1 id="intro-title">Apps I make. For days like yours.</h1>
  <p>I’m Chris, an independent developer making apps for Apple devices.</p>
</section>

{% assign apps = site.pages | where_exp: "app", "app.product" | sort: "app_order" %}
<section class="app-shelf" id="apps" aria-label="Explore my apps">
  {% for app in apps %}
  {% assign product = app.product %}
  <article class="app-edition theme-{{ product.theme }}" aria-labelledby="{{ product.theme }}-title">
    <div class="edition-copy">
      <h2 id="{{ product.theme }}-title"><a href="{{ app.url | relative_url }}">{{ app.title }}</a></h2>
      <p>{{ product.shelf_summary }}</p>
    </div>
    <a class="edition-media{% if product.media_phone %} edition-media-phone{% endif %}" href="{{ app.url | relative_url }}" tabindex="-1" aria-hidden="true">
      <picture>
        <source srcset="{{ product.image_srcset }}" sizes="(max-width: 760px) 94vw, 33vw">
        <img src="{{ product.image | relative_url }}" alt="" width="{{ product.image_width }}" height="{{ product.image_height }}" decoding="async" loading="{% if forloop.first %}eager{% else %}lazy{% endif %}" fetchpriority="{% if forloop.first %}high{% else %}auto{% endif %}">
      </picture>
    </a>
    <div class="edition-details">
      <p class="platforms">{{ product.platforms }}</p>
      <p class="availability">{{ product.availability }}</p>
      <a class="button" href="{{ app.url | relative_url }}">View {{ app.title }}{% include arrow.html %}</a>
    </div>
  </article>
  {% endfor %}
</section>
