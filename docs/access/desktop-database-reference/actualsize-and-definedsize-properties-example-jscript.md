---
title: ActualSize- und DefinedSize-Eigenschaft (Beispiel) (JScript)
TOCTitle: ActualSize and DefinedSize properties example (JScript)
ms:assetid: cf8d6cb6-3446-c193-8774-db41c4d14a2b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250032(v=office.15)
ms:contentKeyID: 48547811
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99c88249180a0c8aeb7baff0e81a7c9e590a5ef4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704287"
---
# <a name="actualsize-and-definedsize-properties-example-jscript"></a><span data-ttu-id="6c18b-102">ActualSize- und DefinedSize-Eigenschaft (Beispiel) (JScript)</span><span class="sxs-lookup"><span data-stu-id="6c18b-102">ActualSize and DefinedSize properties example (JScript)</span></span>

<span data-ttu-id="6c18b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c18b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c18b-p101">In diesem Beispiel werden mit den Eigenschaften [ActualSize](actualsize-property-ado.md) und [DefinedSize](definedsize-property-ado.md) die definierte Größe und die tatsächliche Größe eines Felds angezeigt. Schneiden Sie den folgenden Code aus, fügen Sie ihn in Editor oder einem anderen Texteditor ein, und speichern Sie ihn unter dem Dateinamen **ActualSizeJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="6c18b-p101">This example uses the [ActualSize](actualsize-property-ado.md) and [DefinedSize](definedsize-property-ado.md) properties to display the defined size and actual size of a field. Cut and paste the following code to Notepad or another text editor, and save it as **ActualSizeJS.asp**.</span></span>

```javascript
<!-- BeginActualSizeJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<html> 
 
<head> 
 <title>ActualSize and DefinedSize properties example (JScript)</title> 
<style> 
<!-- 
body { 
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
 
<h1>ADO ActualSize and DefinedSize Properties (JScript)</h1> 
<% 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsSuppliers = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var fld, strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 // Open a recordset on the stores table 
 rsSuppliers.Open("Suppliers", strCnxn); 
 
 // build table headers 
 Response.Write("<table>"); 
 Response.Write('<tr class="thead2"><th>Field Value</th>'); 
 Response.Write("<th>Defined Size</th>"); 
 Response.Write("<th>Actual Size</th></tr>"); 
 
 while (!rsSuppliers.EOF) 
 { 
 // start a new line 
 strMessage = '<tr class="tbody">'; 
 
 // Display the contents of the chosen field with 
 // its defined size and actual size 
 fld = rsSuppliers("CompanyName"); 
 strMessage += '<td align="left">' + fld.Value + "</td>" 
 strMessage += "<td>" + fld.DefinedSize + "</td>"; 
 strMessage += "<td>" + fld.ActualSize + "</td>"; 
 
 // end the line 
 strMessage += "</tr>"; 
 
 // display data 
 Response.Write(strMessage); 
 
 // get next record 
 rsSuppliers.MoveNext; 
 
 } 
 // close the table 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsSuppliers.State == adStateOpen) 
 rsSuppliers.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsSuppliers = null; 
 Cnxn = null; 
 } 
%> 
 
</body> 
 
</html> 
<!-- EndActualSizeJS --> 
 
```

