---
layout: page
title: Publications
permalink: /publications/
---

{% assign pubs = site.publications | sort: "year" | reverse %}
{% for pub in pubs %}
### [{{ pub.title }}]({{ pub.url | relative_url }})
{{ pub.authors | join: ", " }}
*{{ pub.venue }}, {{ pub.year }}*
{% endfor %}