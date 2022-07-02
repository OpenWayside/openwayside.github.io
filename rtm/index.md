---
title: "Code Libraries"
layout: default
---

{%- for lib in site.pages -%}
    title = {{lib.title}}<br />
    id = {{lib.id}}<br />
    dir = {{lib.dir}}<br />
    {% assign dirParts = lib.dir | split: "/" %}
    <pre>{{ dirParts | inspect }}</pre>
    name = {{lib.name}}<br />
    path = {{lib.path}}<br />
    url = {{lib.url}}<br />
    <br /><br /><br /><br /><br /><br /><br /><br /><br />
{%- endfor -%}
