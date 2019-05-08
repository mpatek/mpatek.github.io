---
layout: default
title: Home
---
<h1>Latest Posts</h1>

<ul>
	{% for post in site.posts %}
	<li>
		<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
		<p class="date">{{ post.date | date_to_string }}</p>
		<p class="excerpt">{{ post.excerpt }}</p>
	</li>
	{% endfor %}
</ul>
