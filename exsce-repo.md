---
layout: default
---

# Repository of Executable Scenarios

## Overview

This is the landing page to showcase the metamodels and models developed in the context of the
[SESAME project](https://www.sesame-project.org/) to support the
[Executable Workbench](exsce-workbench.md).

## Metamodels
{% for domain in site.data.metamodels %}
### {{domain.name}}

{{domain.description}}

| File | Description |
|:-----|:-----|{% for file in domain.files %}
|[{{file.name}}]({{file.path}}) | {{file.description}} |{% endfor %}
{% endfor %}

## Tutorials

We created several tutorials showcasing how to create composable models from the metamodels
described above for use with the various tools developed for the
[ExSce Workbench](exsce-workbench.md). These tutorials also demonstrate how the ExSce methodology
can improve composability and promote reuse of these models, showing how they can be extended
to adapt to different variations of the original use case. Our tutorials include:

{% for tool_data in site.data.tutorials %}
### [{{tool_data.tool_name}}]({{tool_data.tool_link}})
{% for tutorial_data in tool_data.tutorials %}
- [{{tutorial_data.title}}]({{tutorial_data.link}}){% endfor %}
{% endfor %}
