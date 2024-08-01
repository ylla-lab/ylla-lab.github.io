---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

Publications with participation of the Lab members (*Lab members highlighted in bold*).

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% include base_path %} {% capture written_year %}'None'{% endcapture %} {% for post in site.publications reversed%} {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %} {% if year != written_year %}
<hr style="height:2px;border:none;color:#333;background-color:#333;" />
<h2>{{year}} </h2>
<hr>
{% capture written_year %}{{ year }}{% endcapture %} {% endif %} {% include archive-single.html %} {% endfor %} 
