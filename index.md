---
layout: default
name: Nightbot Custom Commands
---
# Nightbot Custom Commands

So I made a few custom commands for [Nightbot].

Here are the [Nightbot] commands:

{% for cmdfile in site.static_files %}
    {% if cmdfile.path contains 'cmds' %}
{{ cmdfile.basename }}:

<code>
{% include_relative {{ cmdfile.path }} %}
</code>

    {% endif %}
{% endfor %}

Just copy and paste these into chat and it'll add the command!

[nightbot]: //beta.nightbot.tv/
