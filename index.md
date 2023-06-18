---
layout: default
---

# Executable Scenario Artefacts

## Overview

This is the landing page to showcase the metamodels and models developed in the context of the
[SESAME project](https://www.sesame-project.org/) to support the Executable Workbench.

## Metamodels
{% for domain in site.data.metamodels %}
### {{ domain.name }}

{{domain.description}}

| File | Description |
|:-----|:-----|{% for file in domain.files %}
|[{{ file.name }}]({{ file.path }}) | {{ file.description }} |{% endfor %}

{% endfor %}

### Floor Plan

### Acceptance Criteria

## Tutorials

