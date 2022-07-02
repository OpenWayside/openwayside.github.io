---
title: "Code Libraries"
layout: default
---

{%- for lib in site.pages -%}
    {% assign dirParts = lib.dir | split: "/" %}
    {% if dirParts.size == 2 %}
        {% if dirParts[0] == "rtm" %}
            title = {{lib.title}}<br />
            id = {{lib.id}}<br />
            dir = {{lib.dir}}<br />
            name = {{lib.name}}<br />
            path = {{lib.path}}<br />
            url = {{lib.url}}<br />
            <br /><br /><br /><br /><br /><br /><br /><br /><br />
        {% endif %}
    {% endif %}
{%- endfor -%}
