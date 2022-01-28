---
layout: archive
title: "Lab Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% include base_path %} {% capture written_year %}'None'{% endcapture %} {% for post in site.publications reversed%} {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %} {% if year != written_year %}
<hr>
<h2>{{year}} </h2>
<hr>
{% capture written_year %}{{ year }}{% endcapture %} {% endif %} {% include archive-single.html %} {% endfor %} 
