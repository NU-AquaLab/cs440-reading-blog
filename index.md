---
layout: default
title: Home
---

# {{ site.title }}

**{{ site.author }}** | {{ site.description }}

---

{% assign sorted_posts = site.posts | sort: "date" %}
{% assign current_week = "" %}

{% for post in sorted_posts %}
{% if post.week != current_week %}
{% assign current_week = post.week %}

### Week {{ current_week }}
{% endif %}
- **[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.paper_venue }} · {{ post.date | date: "%B %d" }}
  {% if post.connections %}_Connects to: {% for c in post.connections %}[{{ c.title }}]({{ c.url | relative_url }}){% unless forloop.last %}, {% endunless %}{% endfor %}_{% endif %}
{% endfor %}
