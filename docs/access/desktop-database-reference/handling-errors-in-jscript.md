---
title: Behandeln von Fehlern in JScript
TOCTitle: Handling errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f06584ef752e0be7f68b3f661fbdba50b52cd20e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711693"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="cb866-102">Behandeln von Fehlern in JScript</span><span class="sxs-lookup"><span data-stu-id="cb866-102">Handling errors in JScript</span></span>


<span data-ttu-id="cb866-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb866-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb866-p101">Der Microsoft JScript-Code muss die **Count** -Eigenschaft der **Errors** -Auflistung des **Connection** -Objekts überprüfen. Falls der Wert größer als 0 ist, durchlaufen Sie die Auflistung und drucken Sie die Werte wie in jeder anderen Sprache.</span><span class="sxs-lookup"><span data-stu-id="cb866-p101">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection. If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling example (JScript)</h1> 
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

