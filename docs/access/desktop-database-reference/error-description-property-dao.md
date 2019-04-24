---
title: Error. Description-Eigenschaft (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293504"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="ce44f-102">Error. Description-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="ce44f-102">Error.Description property (DAO)</span></span>


<span data-ttu-id="ce44f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce44f-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="ce44f-104">Returns a descriptive string associated with an error.</span><span class="sxs-lookup"><span data-stu-id="ce44f-104">Returns a descriptive string associated with an error.</span></span> <span data-ttu-id="ce44f-105">This is the default property for the **Error** object.</span><span class="sxs-lookup"><span data-stu-id="ce44f-105">This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce44f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce44f-106">Syntax</span></span>

<span data-ttu-id="ce44f-107">*Ausdruck* . Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce44f-107">*expression* .Description</span></span>

<span data-ttu-id="ce44f-108">*expression* Eine Variable, die ein **Error**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ce44f-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce44f-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce44f-109">Remarks</span></span>

<span data-ttu-id="ce44f-p102">Die **Description**-Eigenschaft umfasst eine kurze Beschreibung zu einem Fehler. Weisen Sie mit dieser Eigenschaft den Benutzer auf einen Fehler hin, den Sie nicht behandeln können oder möchten.</span><span class="sxs-lookup"><span data-stu-id="ce44f-p102">The **Description** property comprises a short description of the error. Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="ce44f-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ce44f-112">Example</span></span>

<span data-ttu-id="ce44f-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span><span class="sxs-lookup"><span data-stu-id="ce44f-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

