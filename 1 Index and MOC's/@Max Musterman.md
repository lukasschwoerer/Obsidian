---

Creation Date: 22.07.2024, 14:07
Company: Muster Firma
tags:
  - Person

---

# Notes

# Samples 
```dataview
table Owner, Measured, embed(link(Cover,"95")) as SampleIMG from "77 Samples" where Owner = link(this.file.name)
```
# Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "3 Meetings" where contains(file.outlinks, [[@Max Musterman]])
SORT file.cday DESC
```