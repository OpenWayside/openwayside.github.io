---
title: "Code Libraries"
layout: default
---

{%- for lib in site.pages -%}
    {%- assign dirParts = lib.dir | split: "/" -%}
    {%- if dirParts.size == 3 -%}
        {%- assign baseDir = dirParts[1] -%}
        {%- assign title = dirParts[2] -%}
        {%- if dirParts[1] == "rtm" -%}      
            BaseDir = {{baseDir}}<br />
            title = {{title}}<br />
            title = {{lib.title}}<br />
            dir = {{lib.dir}}<br />
            name = {{lib.name}}<br />
            path = {{lib.path}}<br />
            url = {{lib.url}}<br />
            <br /><br /><br /><br /><br /><br /><br /><br /><br />
        {%- endif -%}
    {%- endif -%}
{%- endfor -%}
