---
layout: default
name: Nightbot Custom Commands
---
{% capture newline %}
{% endcapture %}
# Nightbot Custom Commands

So I made a few custom commands for [Nightbot].

Here are the [Nightbot] commands:

{% for cmdfile in site.cmds %}
{% assign commands = cmdfile.content | replace: {{ newline }}, "§" | split: "§" %}

{{ cmdfile.name }}:

{% for attr in cmdfile %}
{% if attr contains "cmd_name" %}

<code>
!commands add {{ cmdfile[{{ attr }}] }} {{ commands[{{ forloop.index0 }} ] }}
</code>

{% endif %}
{% endfor %}
{% endfor %}
Just copy and paste these into chat and it'll add the command!

[nightbot]: //beta.nightbot.tv/
