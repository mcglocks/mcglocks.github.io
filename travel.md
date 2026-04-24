---
layout: page
title: Travel
permalink: /travel/
---

Stories and photos from trips past and future.

{% assign travel_posts = site.posts | where_exp: "post", "post.categories contains 'travel'" %}
{% if travel_posts.size > 0 %}
{% for post in travel_posts %}
### [{{ post.title }}]({{ post.url }})
{{ post.date | date: "%B %-d, %Y" }}

{{ post.excerpt }}

---
{% endfor %}
{% else %}
More posts coming soon.
{% endif %}
