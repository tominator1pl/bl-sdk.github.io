---
layout: mod

authors: "apple1417" # Authors of the mod
title: Borderlands Crowd Control # Title of the mod
version: "1.3" # Version of the mod
supported: "BL2 + TPS" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Lets viewers on Twitch spend channel points to affect your game." # A short description of the mod itself.
description: "Lets viewers on Twitch spend channel points to affect your game." # This is set in order to keep the SEO proper
longDescription: "Lets viewers on Twitch spend channel points to affect your game.\n\nInstallation is more involved than other mods, please refer to the [readme](https://github.com/apple1417/bl-sdk-mods/blob/master/CrowdControl/Readme.md).\nThese instructions are included in the download, and are thus not duplicated here to prevent two copies getting out of sync.\n\nA list of the default effects is available [here](https://github.com/apple1417/bl-sdk-mods/blob/master/CrowdControl/Effects.md)." # Description of what the mod can do
categories: ['Gameplay', 'Utility'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/apple1417/bl-sdk-mods/blob/master/CrowdControl/Readme.md"
license: ['GNU GPLv3', 'gpl-3.0'] # License name, link about the license from https://choosealicense.com/

date: 2021-03-21T21:10:58.159961Z # Date of when the generation happened (?)
---
**Contents**
* TOC
{:toc}

## {{page.title}}

Mod by: {{page.authors}}
Current Version: {{page.version}}
  - Mod Page Updated: {{ page.date | date: "%-d %B %Y"}}

<p></p>
### Description

{{page.longDescription | markdownify }}

Currently Supports: `{{page.supported}}`

{% if page.categories.size > 0 %}
Categories:
{% for category in page.categories %}
  * {{category}}
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
Report issues here: [{{page.issues}}]({{page.issues}})
{% endif %}

{% if page.license.size > 0 %}
This mod is licensed using {{page.license[0]}} <sup>[?](https://choosealicense.com/licenses/{{page.license[1]}})
{% endif %}