---
created: <% tp.file.creation_date("DD.MM.YYYY, HH:MM") %>
tag: Meeting
summary: 
---

# Topic 1

# My To Do's


# Participants:
- [[@]]

<% tp.file.move("/3 Meetings/" + tp.date.now("YYYY") + "/" + tp.date.now("MM-MMMM") + "/" + tp.date.now("YYYY-MM-DD") + "-" + await tp.system.prompt("Meeting Name?")) %>
