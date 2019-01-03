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
{% assign commands = cmdfile.content | split: {{ newline }} %}

{% for cmd in commands %}
{{ cmd }}

{% endfor %}

{{ cmdfile.name }}:

{% for attr in cmdfile %}
{% if attr contains "cmd_name" %}
~~~
!commands add {{ cmdfile.attr }} {{ commands[{{ forloop.index0 }} ] }}
~~~

{% endif %}
{% endfor %}
{% endfor %}
Just copy and paste these into chat and it'll add the command!

[nightbot]: //beta.nightbot.tv/
