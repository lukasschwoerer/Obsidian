---
<%*
let items = app.vault.getFiles().filter(file => file.path.includes("4 People"))
let names = items.map(item => item.basename)
let SampleName = await tp.system.prompt("Sample Name?")
let CreationDate = tp.file.creation_date("DD.MM.YYYY, HH:MM")
let CompanyName = await tp.system.prompt("Company Name ?")
let Owner = await tp.system.suggester(names, names)
let SampleMaterial = await tp.system.prompt("Sample Material ?")
SampleName = Owner.substr(Owner.indexOf(" ") + 1) + "_" + SampleName
%>
Creation Date: <% CreationDate %>
Company: <% CompanyName %>
Owner: "[[<% Owner %>]]"
Sample Name: <% SampleName %>
Sample Material: <% SampleMaterial %>
Cover: ""
Measured: false
<% tp.file.move("/77 Samples/" + SampleName) %>
---
# Sample

# Measurements and Findings

# History

# Deadlines
#todo/deadlines

# References
