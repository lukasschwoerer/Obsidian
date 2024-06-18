---
created: <% tp.file.creation_date("DD.MM.YYYY, HH:MM") %>
tags:
  - Note
---
# Heading 1

- 




# References
1. 

<%* tp.file.title = await tp.system.prompt("Note Name?"); %>
<% await tp.file.move("/0 Origin/" + tp.file.title) %>