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
    {%- endif -%}
{%- endfor -%}