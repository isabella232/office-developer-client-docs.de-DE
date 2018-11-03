---
title: Fehlerbehandlung in VBScript
TOCTitle: Handling errors in VBScript
ms:assetid: df8f96d5-b917-ddac-d274-6345b2499bf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250135(v=office.15)
ms:contentKeyID: 48548222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c442472fa30568cc60aec83c2a2de3ecf7ba2f71
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945971"
---
# <a name="handling-errors-in-vbscript"></a><span data-ttu-id="a6bf0-102">Fehlerbehandlung in VBScript</span><span class="sxs-lookup"><span data-stu-id="a6bf0-102">Handling errors in VBScript</span></span>


<span data-ttu-id="a6bf0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6bf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6bf0-104">Es gibt kaum Unterschiede zwischen den in Visual Basic und VBScript verwendeten Methoden.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-104">There is little difference between the methods used in Visual Basic and those used with VBScript.</span></span> <span data-ttu-id="a6bf0-105">Der wichtigste Unterschied ist, dass in VBScript das Konzept der Fehlerbehandlung durch Fortsetzen der Ausführung an einer Marke nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-105">The primary difference is that VBScript does not support the concept of error handling by continuing execution at a label.</span></span> <span data-ttu-id="a6bf0-106">Sie können nicht mit anderen Worten, On Error GoTo in VBScript verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-106">In other words, you cannot use On Error GoTo in VBScript.</span></span> <span data-ttu-id="a6bf0-107">Verwenden Sie stattdessen in VBScript.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-107">Instead, use in VBScript.</span></span> <span data-ttu-id="a6bf0-108">In diesem Fall verwenden Sie On Error Resume Next, und überprüfen Sie **Err.Number** und die **Count** -Eigenschaft der **Errors** -Auflistung, wie im folgenden Beispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="a6bf0-108">Instead, use On Error Resume Next and then check both **Err.Number** and the **Count** property of the **Errors** collection, as shown in the following example:</span></span>

```vb 
 
<!-- BeginErrorExampleVBS --> 
<HTML> 
<HEAD> 
<META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"> 
<TITLE>Error Handling example (VBScript)</TITLE> 
</HEAD> 
<BODY> 
 
<h1>Error Handling example (VBScript)</h1> 
 
<% 
 Dim errLoop 
 Dim strError 
 
 On Error Resume Next 
 
 ' Intentionally trigger an error. 
 Set cnn1 = Server.CreateObject("ADODB.Connection") 
 cnn1.Open "nothing" 
 
 If cnn1.Errors.Count > 0 Then 
 ' Enumerate Errors collection and display 
 ' properties of each Error object. 
 For Each errLoop In cnn1.Errors 
 strError = "Error #" & errLoop.Number & "<br>" & _ 
 " " & errLoop.Description & "<br>" & _ 
 " (Source: " & errLoop.Source & ")" & "<br>" & _ 
 " (SQL State: " & errLoop.SQLState & ")" & "<br>" & _ 
 " (NativeError: " & errLoop.NativeError & ")" & "<br>" 
 If errLoop.HelpFile = "" Then 
 strError = strError & _ 
 " No Help file available" & _ 
 "<br><br>" 
 Else 
 strError = strError & _ 
 " (HelpFile: " & errLoop.HelpFile & ")" & "<br>" & _ 
 " (HelpContext: " & errLoop.HelpContext & ")" & _ 
 "<br><br>" 
 End If 
 Response.Write ("<p>" & strError & "</p>") 
 Next 
 End If 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleVBS --> 
```

