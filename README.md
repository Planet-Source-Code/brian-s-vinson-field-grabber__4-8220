<div align="center">

## Field Grabber


</div>

### Description

Have you ever gotten fat-fingered when trying to get the fields from a "Post" action and scrathed your head trying to figure out where the mistake is? Or pondered over a field input page, trying to figure out all the fields you have so you can add those fields to your request.form statements?

This code eliminates these problems. It grabs the field names and the formats the output in a copy-and-pasteable format so you can spend more time creating and less time trouble-shooting.
 
### More Info
 
Fieldgrabber.asp - a simple, time saving utility.

Create a file named fieldgrabber.asp and paste in this code.

On a form page where you are submitting, make the action

fieldgrabber.asp and the method post. All the field field names

will print out in a copy-and-paste ready format.

Paste the results into the actual page you want to gather

your form info, change the action back to the actual page,

and you're ready.

All the field names from an input page.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Brian S\. Vinson](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/brian-s-vinson.md)
**Level**          |Beginner
**User Rating**    |4.8 (29 globes from 6 users)
**Compatibility**  |ASP \(Active Server Pages\)
**Category**       |[Validation/ Processing](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/validation-processing__4-16.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/brian-s-vinson-field-grabber__4-8220/archive/master.zip)





### Source Code

```
<%
 For Each Item in Request.Form
  For iCount = 1 to Request.Form(Item).Count
 if Request.Form(Item)(iCount) <> "" then
  response.write Item & "=request.form(&quot;" & Item & "&quot;)<br>"
 End if
  Next
 Next
%>
```

