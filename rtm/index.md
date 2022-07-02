---
title: "Code Libraries"
layout: default
---
<b>collections</b>
{%- for collection in site.collections | where: "label", "library" -%}
    {{ collection.label }}<br />
    {%- for post in collection.docs -%}
        {{post.title}} - {{post.url}}<br />
    {%- endfor -%}
{%- endfor -%}
<br />
<br />
<br />
<b>site.library</b>
{%- for lib in site.library -%}
    {{lib.title}} - {{lib.url}}<br />
{%- endfor -%}
<br />
<br />
<br />
<b>site.pages</b>
{%- for lib in site.pages | Where "dir", "/rtm/" -%}
    {{lib.title}} - {{lib.url}} - {{lib.dir}} - {{lib.name}}<br />
{%- endfor -%}
