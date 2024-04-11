---
layout: page
title: Posts
listing: true
---

{% for post in site.posts %}
<article>
	<h2>
		<a href="{{ post.url }}">{{ post.title }}</a>
	</h2>

	<span>
		{{ post.excerpt }}
	</span>

	<ul class="list horizontal">
		{% for category in post.categories %}
		<span class="tag">{{ category }}</span>
		<small>
			<time datetime="{{ post.date }}">{{ post.date | date: "%-d %B %Y" }}</time>
		</small>
		<span class="tag">{{  }}</span>
		{% endfor %}
	</ul>
</article>
{% endfor %}