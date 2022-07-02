---
title: "Code Libraries"
layout: default
---

{%- for lib in site.pages -%}
    {%- assign dirParts = lib.dir | split: "/" -%}
    name = {{lib.name}}<br />
    dirParts = {{dirParts}}<br />
    dirParts.count = {{dirParts.size}}<br />
    {%- if dirParts.size == 3 -%}
        {%- if dirParts[1] == "rtm" -%}
            part2 = {{lib.dirParts[2]}}<br />
            title = {{lib.title}}<br />
            id = {{lib.id}}<br />
            dir = {{lib.dir}}<br />
            name = {{lib.name}}<br />
            path = {{lib.path}}<br />
            url = {{lib.url}}<br />
            <br /><br /><br /><br /><br /><br /><br /><br /><br />
        {%- endif -%}
    {%- endif -%}
{%- endfor -%}
