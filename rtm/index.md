---
title: "Code Libraries"
layout: default
---

{%- for lib in site.pages -%}
    {%- assign dirParts = lib.dir | split: "/" -%}
    {%- if dirParts.size == 3 -%}
        BaseDir = {{dirParts[1]}}<br />
        part2 = {{dirParts[2]}}<br />
        {%- assign lib.title = dirParts[2] -%}
        {%- if dirParts[1] == "rtm" -%}        
            title = {{lib.title}}<br />
            dir = {{lib.dir}}<br />
            name = {{lib.name}}<br />
            path = {{lib.path}}<br />
            url = {{lib.url}}<br />
        {%- endif -%}
    {%- endif -%}
    <br /><br /><br /><br /><br /><br /><br /><br /><br />
{%- endfor -%}
