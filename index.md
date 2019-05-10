---
layout: default
title: Home
---
<h1>Latest Posts</h1>

<ul>
	{% for post in site.posts %}
	<li>
		<h2><a href="{% if post.link %}{{ post.link }}{% else %}{{ post.url }}{% endif %}">{{ post.title }}</a></h2>
		<p class="date">{{ post.date | date_to_string }}</p>
		{% unless post.link %}<p class="excerpt">{{ post.excerpt }}</p>{% endunless %}
	</li>
	{% endfor %}
</ul>
