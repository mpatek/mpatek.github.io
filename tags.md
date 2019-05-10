---
layout: default
title: Tags
---
<h1>Tags</h1>

<ul>
	{% capture temptags %}
		{% for tag in site.tags %}
			{{ tag[0] }}
		{% endfor %}
	{% endcapture %}
	{% assign tags = temptags | split:' ' | sort %}
	{% for tag in tags %}
		<li><a href="/tag/{{ tag }}.html">{{ tag }}</a></li>
	{% endfor %}
</ul>
