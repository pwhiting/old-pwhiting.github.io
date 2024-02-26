---
layout: page
title: Blog Archive
---
{% for tag in site.tags %}
  <ul style="list-style-type:none;padding:0;margin:0;">
    {% for post in tag[1] reversed %}
     <li>
       {{ post.date | date_to_string }} &mdash;
       <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
