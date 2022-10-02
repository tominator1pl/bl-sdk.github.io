---
layout: main

authors: "ZetaDæmon" # Authors of the mod
title: Difficulty Modes # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2 + TPS + AoDK" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Replaces BAR with a difficulty mode that can be changed in the options." # A short description of the mod itself.
description: "Replaces BAR with a difficulty mode that can be changed in the options." # This is set in order to keep the SEO proper
longDescription: "Replaces BAR with a difficulty mode that can be changed in the options." # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: ['Structs >= 1.0', 'Enums >= 1.1'] # Requirements for the given mod
requirementTitles: ['Structs', 'Enums'] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/ZetaDaemon/bl-sdk-mods/raw/main/DifficultyModes/DifficultyModes.zip"
source: "https://github.com/ZetaDaemon/bl-sdk-mods/" # Link to source code
license: ['GNU GPLv3', 'https://choosealicense.com/licenses/gpl-3.0'] # License name, link about the license from https://choosealicense.com/

---
**Contents**
* TOC
{:toc}

## {{page.title}}

Mod by: {{page.authors}}
Current Version: {{page.version}}

<p></p>
### Description

{{page.longDescription | markdownify }}

Currently Supports: `{{page.supported}}`

{% if page.categories.size > 0 %}
Categories:
{% for category in page.categories %}
  * [{{category}}](/types/{{category}})
{% endfor %}
<p></p>
{% endif %}

{% if page.requirements.size > 0 %}
### Requirements

{% for requirement in page.requirements %}

{% assign reqName = page.requirementTitles[forloop.index0] %}

{% for mod in site.mods %}

{% assign modName = mod.path | remove_first: '_mods/' %}
{% assign xz = reqName | append: '.md' %}

{% if modName == xz %}
* [{{ requirement }}]( {{ reqName | relative_url | prepend: '/mods'}} ) <sup>[(Direct Download)]({{mod.download}})</sup>
{% endif %}
{% endfor %}

{% endfor %}
<p></p>
{% endif %}

### Links

{% if page.download != "" %}
You can download {{page.title}} here: [Download Link]({{page.download}})
{% endif %}

{% if page.issues != "" %}
Report issues here: [Issue Tracker]({{page.issues}})
{% endif %}

{% if page.source != "" %}
View the source code here: [Source Code]({{page.source}})
{% endif %}

{% if page.license.size > 0 %}
This mod is licensed using {{page.license[0]}} <sup>[?]({{page.license[1]}})</sup>
{% endif %}