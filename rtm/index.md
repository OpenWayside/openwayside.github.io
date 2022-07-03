---
title: "Code Libraries"
layout: default
---
{%- for lib in site.pages -%}
    {%- assign dirParts = lib.dir | split: "/" -%}
    {%- if dirParts.size == 3 -%}
        {%- assign baseDir = dirParts[1] -%}
        {%- assign title = dirParts[2] -%}
        {%- if baseDir == "rtm" -%}      
            <a href="{{lib.url}}">{{title}}</a><br />
        {%- endif -%}
    {%- elsif dirParts.size == 4 -%}
        {%- assign baseDir = dirParts[1] -%}
        {%- assign title = dirParts[2] -%}
        {%- assign file = dirParts[3] -%}
        {%- if baseDir == "rtm" -%}
            {%- if file == "index.html" or file == "index.md" or file == "readme.md" -%}  
                <a href="{{lib.url}}">{{title}}</a><br />
            {%- endif -%}
        {%- endif -%}
    {%- endif -%}
{%- endfor -%}