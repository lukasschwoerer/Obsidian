---
created: <% tp.file.creation_date("DD.MM.YYYY, HH:MM") %>
tag: Daily
---
<%*
let FileDateYesterday = moment(tp.file.title,'YYYY-MM-DD-dddd').subtract(1,'d').format('YYYY-MM-DD-dddd')
let FileDateTomorrow = moment(tp.file.title,'YYYY-MM-DD-dddd').add(1,'d').format('YYYY-MM-DD-dddd')

let MonthYesterday = moment(tp.file.title, 'YYYY-MM-DD-dddd').subtract(1, 'd').format('MM-MMMM')
let MonthTomorrow = moment(tp.file.title, 'YYYY-MM-DD-dddd').add(1, 'd').format('MM-MMMM')

let YearYesterday =moment(tp.file.title, 'YYYY-MM-DD-dddd').subtract(1, 'd').format('YYYY')
let YearTomorrow = moment(tp.file.title, 'YYYY-MM-DD-dddd').add(1, 'd').format('YYYY')
tR += "<<[[2 Periodic Notes/0 Daily Notes/" + YearYesterday + "/" + MonthYesterday + "/" + FileDateYesterday + "|Yesterday]]" + " | " + "[[2 Periodic Notes/0 Daily Notes/" + YearTomorrow + "/" + MonthTomorrow + "/" + FileDateTomorrow + "|Tomorrow]]>>"
%>
# High Prio Tasks
```dataview
TASK
WHERE !completed
 AND contains(text, "🔺")
SORT text ASC
```
# Notes
- 

# To Do's
#todo/