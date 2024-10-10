---
layout: page
title: Our Team
description: A listing of all our leadership members.
---

# Leadership

//Leadership information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.

## Chairs

{% assign chairs = site.staffers | where: 'role', 'Chair' %}
{% for staffer in chairs %}
{{ staffer }}
{% endfor %}

{% assign leads = site.staffers | where: 'role', 'Lead' %}
{% assign num_leads = leads | size %}
{% if num_leads != 0 %}
## Leads

{% for staffer in leads %}
{{ staffer }}
{% endfor %}
{% endif %}
