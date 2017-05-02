---
layout: page
title: Open Geneva Hackathons
permalink: /test/
---


{% for hack in site.data.hackathons %}
{% if hack.display == true %}
  <h3>

  {% if hack.logo != '' %}
  <a href="{{hack.url}}" target="_blank"><img src="{{ site.baseurl }}/{{hack.logo}}" height="60" alt="" class="imgspace" /></a>
  {% endif %}
<a href="{{hack.url}}" target="_blank">{{ hack.title }}</a>
</h3>

Date : {{ hack.date}}<br>
Lieu : {{ hack.location}}<br>
Adresse : {{ hack.address}}<br>
Salle : {{ hack.room}}<br>
Contact : <a href="mailto: {{hack.contact}}"> {{hack.contact}}</a><br>
Twitter : <a href="https://twitter.com/{{hack.twitter}}" target="_blank">{{hack.twitter}}</a>



{% if hack.image != '' %}
<img src="{{ site.baseurl }}/{{ hack.image}}" width="300" alt="" class="imgspace" />
{% endif %}


{% if hack.wiki != '' %}
<h4><a href="{{hack.wiki}}" target="_blank">wiki page</a></h4>
{% endif %}
<br><br>
{% endif %}
{% endfor %}
