---
layout: default
---

# Repository of Executable Scenarios

This is the landing page for the Repository of Executable Scenarios, which consists of
metamodels and models created during the development and application of tools in the
[Executable Workbench](exsce-workbench.md) and
[ExSce Management](https://github.com/hbrs-sesame/exsce_management) to support the
[ExSce Concept and Methodology](terminology.md). In the following sections, we first
present the different metamodels developed for ExSce, organized by their respective
domains. Afterwards, we list the tutorials showcasing how these metamodels can be
composed to create composable models and the various transformations enabled by
our tools to support different use cases.

## Metamodels
{% for domain in site.data.metamodels %}
### {{domain.name}}

{{domain.description}}

| File | Description |
|:-----|:-----|{% for file in domain.files %}
|[{{file.name}}]({{file.path}}) | {{file.description}} |{% endfor %}
{% endfor %}

## Tutorials

The development of tools in the [ExSce Workbench](exsce-workbench.md) produces many artefacts,
either as compositions of our metamodels or from various transformations to support different
use cases. Finding a single structure to organize these artefacts can therefore be challenging,
since they often involve the complex interplay of different domains and support different
stakeholder activities. As such, we present our models through a list of tutorials showcasing
how they can be composed and transformed to serve specific stakeholder workflows. The tutorials
can then link to our models while describing how they are used in the context of each workflow.
Many of our models are hosted on the [hbrs-sesame/models](https://github.com/secorolab/models)
repository, for which a [landing page](https://secorolab.github.io/models/) is also available.
Our tutorials include:

{% for tool_data in site.data.tutorials %}
### [{{tool_data.tool_name}}]({{tool_data.tool_link}})
{% for tutorial_data in tool_data.tutorials %}
- [{{tutorial_data.title}}]({{tutorial_data.link}}){% endfor %}
{% endfor %}
