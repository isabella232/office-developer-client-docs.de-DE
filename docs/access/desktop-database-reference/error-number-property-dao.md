---
title: Error.Number-Eigenschaft (DAO)
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
ms.openlocfilehash: 95d814bb613b848f65b61cd342d2918fbbd2fea2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928341"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="764ba-102">Error.Number-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="764ba-102">Error.Number property (DAO)</span></span>


<span data-ttu-id="764ba-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="764ba-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="764ba-104">Gibt einen nummerischen Wert zurück, der einen Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="764ba-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="764ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="764ba-105">Syntax</span></span>

<span data-ttu-id="764ba-106">*Ausdruck* . Anzahl</span><span class="sxs-lookup"><span data-stu-id="764ba-106">*expression* .Number</span></span>

<span data-ttu-id="764ba-107">*Ausdruck* Eine Variable, die ein **Error** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="764ba-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="764ba-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="764ba-108">Remarks</span></span>

<span data-ttu-id="764ba-p101">Mit der **Number**-Eigenschaft können Sie den aufgetretenen Fehler ermitteln. Der Wert der Eigenschaft ist eine eindeutige Fehlernummer, die eine Fehlerbedingung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="764ba-p101">Use the **Number** property to determine the error that occurred. The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="764ba-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="764ba-111">Example</span></span>

<span data-ttu-id="764ba-112">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="764ba-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

