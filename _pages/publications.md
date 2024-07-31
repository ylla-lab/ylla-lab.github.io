---
layout: archive
title: "Lab Publications"
permalink: /publications/
author_profile: true
---

Publications with participation of the Lab members (lab members highlighted in bold).

{% if https://scholar.google.es/citations?user=B4f5UDgAAAAJ&hl=ca %}
  You can also find my articles on <u><a href="{{https://scholar.google.es/citations?user=B4f5UDgAAAAJ&hl=ca}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% include base_path %} {% capture written_year %}'None'{% endcapture %} {% for post in site.publications reversed%} {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %} {% if year != written_year %}
<hr style="height:2px;border:none;color:#333;background-color:#333;" />
<h2>{{year}} </h2>
<hr>
{% capture written_year %}{{ year }}{% endcapture %} {% endif %} {% include archive-single.html %} {% endfor %} 
