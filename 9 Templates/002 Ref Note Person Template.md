---
<%*
let PersonName = await tp.system.prompt("Name?")
let CreationDate = tp.file.creation_date("DD.MM.YYYY, HH:MM")
let CompanyName = await tp.system.prompt("Company?")
%>
Creation Date: <% CreationDate %>
Company: <% CompanyName %>
tags:
  - Person
<% await tp.file.move("/5 People/" + "@" + PersonName) %>
---

# Notes

# Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "3 Meetings" where contains(file.outlinks, [[<% "@" + PersonName %>]])
SORT file.cday DESC
```