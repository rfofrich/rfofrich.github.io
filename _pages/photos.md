---
layout: page
title: Photography
permalink: /photography/
nav: true
---

Apart from life as a researcher, I am an amateur photographer with a passion for capturing the natural world. From landscapes, ecosystems, and the places where my life takes me. All photos are my own.

<div class="row mt-4">
  {% assign photos = site.static_files | where_exp: "file", "file.path contains '/assets/img/photos/'" %}
  {% for photo in photos %}
    {% if photo.extname == '.jpg' or photo.extname == '.jpeg' or photo.extname == '.png' or photo.extname == '.JPG' or photo.extname == '.JPEG' %}
    <div class="col-sm-6 col-md-4 mb-4">
      <a href="{{ photo.path | relative_url }}" target="_blank">
        <img src="{{ photo.path | relative_url }}" class="img-fluid rounded" alt="Photography by Robert Fofrich" style="object-fit: cover; width: 100%; height: 250px;" />
      </a>
    </div>
    {% endif %}
  {% endfor %}
</div>
