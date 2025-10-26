---
title: "Publications"
layout: page
permalink: /publications/
---

<h2>Selected Publications</h2>
<p>(Note: * indicates equal contribution.)</p>

{% assign pubs = site.pages | where: "title", "About Me" | first | map: "publications" | first %}

{% for pub in pubs %}
<div style="display: flex; align-items: flex-start; margin-bottom: 30px;">
    <img src="{{ pub.img }}" alt="Paper Image" style="width: 150px; margin-right: 20px;">
    <div>
        <strong>{{ pub.title }}</strong><br>
        {{ pub.authors }}<br>
        <em>{{ pub.journal }}</em><br>
        <a href="{{ pub.paper_url }}" target="_blank">Paper</a> | <a href="{{ pub.code_url }}" target="_blank">Code</a>
    </div>
</div>
{% endfor %}
