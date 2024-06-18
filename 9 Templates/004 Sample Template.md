---
<%*
let SampleName = await tp.system.prompt("Sample Name?")
let CreationDate = tp.file.creation_date("DD.MM.YYYY, HH:MM")
let CompanyName = await tp.system.prompt("Company Name ?")
let Owner = await tp.system.prompt("Owner ?")
let SampleMaterial = await tp.system.prompt("Sample Material ?")
%>
Creation Date: <% CreationDate %>
Company: <% CompanyName %>
Owner: <% Owner %>
Sample Name: <% SampleName %>
Sample Material: <% SampleMaterial %>
Image Path:
<% tp.file.move("/77 Samples/" + SampleName) %>
---
# Sample

## Image



# Deadlines
#todo/deadlines

# References
