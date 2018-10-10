---
title: Error.Number Property (DAO)
TOCTitle: Number Property
ms:assetid: 2fb94dca-f990-04f8-bbd2-9919d28de75a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192259(v=office.15)
ms:contentKeyID: 48544013
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053363
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8e7f5f4b6a0d4fa12be35a20f0a17717fdef1062
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473104"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="24683-102">Error.Number Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="24683-102">Error.Number Property (DAO)</span></span>


<span data-ttu-id="24683-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="24683-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="24683-104">Gibt einen nummerischen Wert zurück, der einen Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="24683-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="24683-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24683-105">Syntax</span></span>

<span data-ttu-id="24683-106">*Ausdruck* . Anzahl</span><span class="sxs-lookup"><span data-stu-id="24683-106">*expression* .Number</span></span>

<span data-ttu-id="24683-107">*Ausdruck* Eine Variable, die ein **Error** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="24683-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24683-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24683-108">Remarks</span></span>

<span data-ttu-id="24683-p101">Mit der **Number**-Eigenschaft können Sie den aufgetretenen Fehler ermitteln. Der Wert der Eigenschaft ist eine eindeutige Fehlernummer, die eine Fehlerbedingung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="24683-p101">Use the **Number** property to determine the error that occurred. The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="24683-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="24683-111">Example</span></span>

<span data-ttu-id="24683-112">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="24683-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

