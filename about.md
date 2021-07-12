---
layout: dark
title: About
example: This is an example value.
---



## About About Pages

The About page is a common convention found on websites.
It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used

This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

{% include demo.html %}

{% for test in site.data.tests %}
- The {{ test.name }}
{% endfor %}

## header 2
{% for test in site.data.tests %}
{% if test.size == "large" %}- <strong style="color: {{ test.color }}">{{ test.name }} </strong>
{% else %}- <small>{{ test.name }}</small>
{% endif %}
{% endfor %}


## header 3
{% assign small_tests = site.data.tests | where: "size", "small" %}
{% for test in small_tests %}
- {{ test.name | upcase }}
{% endfor %}
