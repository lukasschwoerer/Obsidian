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
<% await tp.file.move("/4 People/" + "@" + PersonName) %>
---

# Notes

# Samples 
```dataview
table Owner, Measured, embed(link(Cover,"95")) as SampleIMG from "77 Samples" where Owner = link(this.file.name)
```
# Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "3 Meetings" where contains(file.outlinks, [[<% "@" + PersonName %>]])
SORT file.cday DESC
```