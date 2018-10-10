---
title: Fehlerbehandlung in JScript
TOCTitle: Handling Errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2a2fadb9f7f377782ce7cc7d45820769927b4f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474773"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="8a3ef-102">Fehlerbehandlung in JScript</span><span class="sxs-lookup"><span data-stu-id="8a3ef-102">Handling Errors in JScript</span></span>


<span data-ttu-id="8a3ef-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a3ef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8a3ef-p101">Der Microsoft JScript-Code muss die **Count** -Eigenschaft der **Errors** -Auflistung des **Connection** -Objekts überprüfen. Falls der Wert größer als 0 ist, durchlaufen Sie die Auflistung und drucken Sie die Werte wie in jeder anderen Sprache.</span><span class="sxs-lookup"><span data-stu-id="8a3ef-p101">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection. If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling Example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling Example (JScript)</h1> 
<% 
 var cnn1 = Server.CreateObject("ADODB.Connection"); 
 var errLoop = Server.CreateObject("ADODB.Error"); 
 var strError = new String; 
 
 try 
 { 
 // Intentionally trigger an error. 
 cnn1.Open("nothing"); 
 } 
 catch(e) 
 { 
 Response.Write(e.message); 
 } 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleJS --> 
```

