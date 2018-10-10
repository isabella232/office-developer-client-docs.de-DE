---
title: Execute-, Requery- und Clear-Methoden (Beispiel) (JScript)
TOCTitle: Execute, Requery, and Clear Methods Example (JScript)
ms:assetid: 3c1f1913-f168-b8a9-8791-f4a0b1aa8273
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249157(v=office.15)
ms:contentKeyID: 48544306
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03462ce181dd3dadade6dc63a6a0d4cc2c06e08c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474298"
---
# <a name="execute-requery-and-clear-methods-example-jscript"></a>Execute-, Requery- und Clear-Methoden (Beispiel) (JScript)


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird die Ausführung der **Execute** -Methode aus einem [Command](command-object-ado.md)-Objekt und einem [Connection](connection-object-ado.md)-Objekt dargestellt. Außerdem wird die [Requery](requery-method-ado.md)-Methode zum Abrufen von aktuellen Daten in einem [Recordset](recordset-object-ado.md)-Objekt und die [Clear](clear-method-ado.md)-Methode zum Löschen des Inhalts der [Errors](errors-collection-ado.md)-Auflistung verwendet. (Auf die **Errors** -Auflistung wird mithilfe des **Connection** -Objekts der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des [Recordset](recordset-object-ado.md)-Objekts zugegriffen.) Benennen Sie die Datei **ExecuteJS.asp**.

```javascript 
 
<!-- BeginExecuteJS --> 
<%@LANGUAGE="JScript"%> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<% 
 strLastName = new String(Request.Form("AuthorLName")); 
 
 if (strLastName.indexOf("undefined") > -1) 
 strLastName = ""; 
%> 
 
<html> 
 
<head> 
<title>Execute, Requery and Clear Methods Example (JScript)</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="White"> 
<h1>Execute, Requery and Clear Methods Example (JScript)</h1> 
<% 
 if (strLastName.length > 0) 
 { 
 // command and recordset variables 
 var Connect = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var Cnxn = Server.CreateObject("ADODB.Connection"); 
 var cmdAuthor = Server.CreateObject("ADODB.Command"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor2 = Server.CreateObject("ADODB.Recordset"); 
 var SQLAuthor2, strMessage, strMessage2; 
 var Err, ErrCount; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(Connect); 
 
 // command object parameters 
 cmdAuthor.CommandText = "SELECT * FROM Authors WHERE au_lname = ?"; 
 cmdAuthor.Parameters.Append(cmdAuthor.CreateParameter("Last Name", adChar, adParamInput, 20, strLastName)); 
 cmdAuthor.ActiveConnection = Cnxn; 
 
 // recordset from command.execute 
 rsAuthor = cmdAuthor.Execute(); 
 
 // recordset from connection.execute 
 SQLAuthor2 = "SELECT * FROM Authors"; 
 rsAuthor2 = Cnxn.Execute(SQLAuthor2); 
 
 // check for errors 
 ErrCount = Cnxn.errors.count; 
 if(ErrCount !== 0) //write the errors 
 { 
 for(Err = 0; Err = ErrCount; Err++){ 
 Err = Cnxn.errors.item; 
 Response.Write(Err); 
 } 
 // clean out any existing errors 
 Cnxn.Errors.Clear; 
 } 
 
 // show the data 
 Response.Write("<HR><HR>"); 
 
 // first recordset 
 Response.Write("<b>Command.Execute results</b>") 
 while (!rsAuthor.EOF) 
 { 
 // build output string by starting a new line 
 strMessage = "<P>"; 
 strMessage += "<br>"; 
 
 // recordset data 
 strMessage += rsAuthor("au_fname") + " "; 
 strMessage += rsAuthor("au_lname") + " "; 
 
 // end the line 
 strMessage += "</P>"; 
 
 // show the results 
 Response.Write(strMessage); 
 
 // get next record 
 rsAuthor.MoveNext; 
 } 
 
 Response.Write("<HR><HR>"); 
 
 // second recordset 
 Response.Write("<b>Connection.Execute results</b>") 
 while (!rsAuthor2.EOF) 
 { 
 // start a new line 
 strMessage2 = "<P>"; 
 
 // first and last name are in first column 
 strMessage2 += rsAuthor2("au_fname") + " " 
 strMessage2 += rsAuthor2("au_lname") + " "; 
 
 // end the line 
 strMessage2 += "</P>"; 
 
 // show results 
 Response.Write(strMessage2); 
 
 // get next record 
 rsAuthor2.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsAuthor.State == adStateOpen) 
 rsAuthor.Close; 
 if (rsAuthor2.State == adStateOpen) 
 rsAuthor2.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsAuthor1 = null; 
 rsAuthor2 = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="ExecuteJS.asp" id=form1 name=form1> 
 <p align="left">Enter last name of author to find (e.g., Ringer): <input type="text" name="AuthorLName" size="40"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
</body> 
 
</html> 
<!-- EndExecuteJS --> 
 
```
