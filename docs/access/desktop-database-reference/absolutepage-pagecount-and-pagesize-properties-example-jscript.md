---
<<<<<<< HEAD-Titel: AbsolutePage-, PageCount- und PageSize-Eigenschaften (Beispiel) (JScript) TOCTitle: AbsolutePage-, PageCount- und PageSize-Eigenschaften (Beispiel) (JScript) Ms:assetid: 6df29022-16f2-c7d8-d45b-b9998e929030 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249434(v=office.15) Ms:contentKeyID: 48545506 ms.date: 09/18/2015 Mtps_version: Office. 15
---

# <a name="absolutepage-pagecount-and-pagesize-properties-example-jscript"></a>AbsolutePage-, PageCount- und PageSize-Eigenschaft (Beispiel) (JScript)

**Betrifft**: Access 2013 | Office 2013

<a name="this-example-demonstrates-the-absolutepage-pagecount-and-pagesize-properties-cut-and-paste-the-following-code-to-notepad-or-another-text-editor-and-save-it-as-absolutepagejsasp"></a>Dieses Beispiel veranschaulicht die AbsolutePage-, PageCount- und PageSize-Eigenschaften. Schneiden Sie aus und fügen Sie den folgenden Code in Editor oder einem anderen Texteditor, und speichern Sie es als **AbsolutePageJS.asp**.
=======
Titel: AbsolutePage-, PageCount- und PageSize-Eigenschaften (Beispiel) (JScript) TOCTitle: AbsolutePage-, PageCount- und PageSize-Eigenschaften (Beispiel) (JScript) Ms:assetid: 6df29022-16f2-c7d8-d45b-b9998e929030 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249434(v=office.15) Ms:contentKeyID: 48545506 ms.date: 10/17/2018 Mtps_version: Office. 15
---

# <a name="absolutepage-pagecount-and-pagesize-properties-example-jscript"></a>AbsolutePage-, PageCount- und PageSize-Eigenschaften (Beispiel) (JScript)

**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel werden mithilfe der Eigenschaften [AbsolutePage](absolutepage-property-ado.md), [PageCount](pagecount-property-ado.md) und [PageSize](pagesize-property-ado.md) Namen und Einstellungsdaten aus der ***Employees***-Tabelle angezeigt. Es werden jeweils fünf Datensätze dargestellt. Schneiden Sie aus und fügen Sie den folgenden Code in Editor oder einem anderen Texteditor, und speichern Sie es als **AbsolutePageJS.asp**.
>>>>>>> master

```javascript
<!-- BeginAbsolutePageJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<title>AbsolutePage, PageSize, and PageSize Properties (JScript)</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead2 { 
 background-color: #800000; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.tbody { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="White"> 
<h1>AbsolutePage, PageSize, and PageSize Properties (JScript)</h1> 
<% 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var strMessage, iRecord, iPageCount; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 // Open a recordset on the Employee table using 
 // a client-side cursor to enable AbsolutePage property. 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("employees", strCnxn, adOpenStatic, adLockOptimistic, adCmdTable); 
 
 // Set PageSize to five to display names and hire dates of five employees at a time 
 rsEmployee.PageSize = 5; 
 iPageCount = rsEmployee.PageCount; 
 
 // Write header information to the document 
 Response.Write('<p align="center">There are ' + iPageCount); 
 Response.Write(" pages, each containing "); 
 Response.Write(rsEmployee.PageSize + " or fewer records.</p>"); 
 Response.Write('<table border="0" align="center">'); 
 Response.Write('<tr class="thead2">'); 
 Response.Write("<th>Page</th><th>Name</th><th>Hire Date</th></tr>"); 
 
 for (var i=1; i<=iPageCount; i++) 
 { 
 rsEmployee.AbsolutePage = i; 
 
 for (iRecord = 1; iRecord <= rsEmployee.PageSize; iRecord++) 
 { 
 strMessage = ""; 
 
 // Start a new table row. 
 strMessage = '<tr class="tbody">'; 
 
 // First column in row contains page number on 
 // first record of each page. Otherwise, the column 
 // contains a non-breaking space. 
 if (iRecord == 1) 
 strMessage += "<td>Page " + i + " of " + rsEmployee.PageCount + "</td>" 
 else 
 strMessage += "<td>&nbsp;</td>"; 
 
 // First and last name are in first column. 
 strMessage += "<TD>" + rsEmployee.Fields("FirstName") + " "; 
 strMessage += rsEmployee.Fields("LastName") + " " + "</td>"; 
 
 // Hire date in second column. 
 strMessage += "<td>" + rsEmployee.Fields("HireDate") + "</td>"; 
 
 // End the row. 
 strMessage += "</tr>"; 
 
 // Write line to document. 
 Response.Write(strMessage); 
 
 // Get next record. 
 rsEmployee.MoveNext; 
 
 if (rsEmployee.EOF) 
 break; 
 } 
 } 
 
 // Finish writing table. 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsEmployee = null; 
 Cnxn = null; 
 } 
%> 
 
</body> 
 
</html> 
<!-- EndAbsolutePageJS --> 
```
