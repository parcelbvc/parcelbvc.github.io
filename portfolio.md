---
layout: home
---

# Portfolio
{% assign posts = site.posts %}

{%- if posts.size > 0 -%}
    {%- if page.list_title -%}
        ## {{ page.list_title }}
    {%- endif -%}
    <ul class="post-list">
        {%- for post in posts -%}
            <li>
                <p class="post-title"><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></p>
                <span class="post-founders">{{ post.founders }}</span>
            </li>
        {%- endfor -%}
    </ul>
{%- endif %}
