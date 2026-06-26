---
layout: default
title: Shark Strike Networks Blog
---
<header>
  <div>
    <a href="{{ "/" | prepend: site.baseurl | replace: '//', '/' }}">
    {% assign owner_first_name = site.owner | split: " " %}
    <h1>{{ owner_first_name[0] | downcase }}@home:~$</h1>
    </a>
    <div class="header-links">
        <a href="{{ "/archive" | prepend: site.baseurl | replace: '//', '/' }}"><h2 class="header-link">Archive</h2></a>
        <a href="{{ "/about" | prepend: site.baseurl | replace: '//', '/' }}"><h2 class="header-link">About</h2></a>
        <a href="{{ "/atom.xml" | prepend: site.baseurl | replace: '//', '/' }}"><h2 class="header-link">RSS</h2></a>
    </div>
  </div>
</header>

[Link to another page](./test.md)

<ul>
    {% for post in paginator.posts %}
        <li>
            <h2><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></h2>
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
            <p>{{ post.content | strip_html | truncatewords:50 }}</p>
        </li>
    {% endfor %}
</ul>