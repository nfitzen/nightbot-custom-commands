---
layout: default
name: Nightbot Custom Commands
---
{% assign cmd_files = site.static_files | where: "cmd", true %}
# Nightbot Custom Commands

So I made a few custom commands for [Nightbot].

Here are the [Nightbot] commands:
{% for cmdfile in cmd_files %}
    {{cmdfile.basename}}:
    ```{{ cmdfile.content }}```
{% endfor %}

Just copy and paste these into chat and it'll add the command!

[nightbot]: //beta.nightbot.tv/
