---
title: "Code Libraries"
layout: default
---

{%- for lib in site.pages -%}
    {%- assign dirParts = lib.dir | split: "/" -%}
    name = {{lib.name}}<br />
    dirParts.count = {{dirParts.size}}<br />
    {%- if dirParts.size == 3 -%}
        part0 = {{dirParts[0]}}<br />
        part1 = {{dirParts[1]}}<br />
        part2 = {{dirParts[2]}}<br />
        {%- if dirParts[1] == "rtm" -%}        
            title = {{lib.title}}<br />
            id = {{lib.id}}<br />
            dir = {{lib.dir}}<br />
            name = {{lib.name}}<br />
            path = {{lib.path}}<br />
            url = {{lib.url}}<br />
        {%- endif -%}
    {%- endif -%}
    <br /><br /><br /><br /><br /><br /><br /><br /><br />
{%- endfor -%}
