---
layout: default
name: Nightbot Custom Commands
---
# Nightbot Custom Commands

So I made a few custom commands for [Nightbot].

Here are the [Nightbot] commands:

{% for cmdfile in site.cmds %}
{{ cmdfile.basename }}:

<code>
{% include {{ cmdfile.name }} %}
</code>

{% endfor %}

Just copy and paste these into chat and it'll add the command!

[nightbot]: //beta.nightbot.tv/
