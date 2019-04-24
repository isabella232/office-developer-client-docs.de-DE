---
title: Error. Source-Eigenschaft (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 79c5fa1e01bbb6bce4f2cef705f23f3259bf0678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293441"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="5cbce-102">Error. Source-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="5cbce-102">Error.Source property (DAO)</span></span>


<span data-ttu-id="5cbce-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cbce-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="5cbce-104">Gibt den Namen des Objekts zurück, das den Fehler ursprünglich erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="5cbce-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cbce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cbce-105">Syntax</span></span>

<span data-ttu-id="5cbce-106">*Ausdruck* . Quelle</span><span class="sxs-lookup"><span data-stu-id="5cbce-106">*expression* .Source</span></span>

<span data-ttu-id="5cbce-107">*expression* Eine Variable, die ein **Error**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5cbce-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cbce-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5cbce-108">Remarks</span></span>

<span data-ttu-id="5cbce-p101">Der Wert der **Source**-Eigenschaft ist gewöhnlich der Klassenname oder die Programm-ID des Objekts. Mit der **Source**-Eigenschaft können Sie dem Benutzer Informationen darüber liefern, ob der Code Fehler behandeln kann, die von einem Objekt in einer anderen Anwendung erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="5cbce-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="5cbce-111">Wenn Sie beispielsweise auf Microsoft Excel zugreifen und einen Fehler "Division durch Null" generiert haben, wird in Microsoft Excel **Error. Number** auf den Microsoft Excel-Code für diesen Fehler festgelegt und die **Source** -Eigenschaft auf Excel. Application festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5cbce-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="5cbce-112">Wenn ein Fehler von einem anderen von Microsoft Excel aufgerufenen Objekt erzeugt wird, fängt Microsoft Excel den Fehler ab und setzt **Error.Number** dennoch auf den Microsoft Excel-Code.</span><span class="sxs-lookup"><span data-stu-id="5cbce-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="5cbce-113">Die anderen Eigenschaften des **Error**-Objekts (einschließlich **Source**) behalten jedoch ihre Werte, die von dem Objekt festgelegt wurden, das den Fehler erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="5cbce-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="5cbce-114">Die **Source**-Eigenschaft enthält immer den Namen des Objekts, das den Fehler ursprünglich erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="5cbce-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="5cbce-p103">Basierend auf der gesamten Fehlerdokumentation können Sie Code schreiben, der den Fehler angemessen behandelt. Wenn Ihre Fehlerbehandlung fehlschlägt, können Sie den Fehler mithilfe der Informationen des **[Error](error-object-dao.md)** -Objekts für den Benutzer beschreiben. Hierzu können Sie die **Source**-Eigenschaft und die anderen **Error**-Eigenschaften verwenden, um den Benutzer darüber zu informieren, welches Objekt den Fehler ursprünglich verursacht hat, eine Fehlerbeschreibung zu liefern usw.</span><span class="sxs-lookup"><span data-stu-id="5cbce-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <span data-ttu-id="5cbce-117">[!HINWEIS] Das **On Error Resume Next**-Konstrukt ist möglicherweise **On Error GoTo** vorzuziehen, wenn Fehler behandelt werden, die während des Zugriffs auf andere Objekte erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="5cbce-117">The **On Error Resume Next** construct may be preferable to **On Error GoTo** when dealing with errors generated during access to other objects.</span></span> <span data-ttu-id="5cbce-118">Wenn das **Error**-Objekt nach jeder Interaktion mit einem Objekt überprüft wird, kann jeder Zweifel darüber aus dem Weg geräumt werden, auf welches Objekt der Code beim Auftreten des Fehlers zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="5cbce-118">Checking the **Error** object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred.</span></span> <span data-ttu-id="5cbce-119">Auf diese Weise wissen Sie, welches Objekt den Fehlercode in **Error.Number** geschrieben und welches Objekt den Fehler ursprünglich erzeugt hat (**Error.Source**).</span><span class="sxs-lookup"><span data-stu-id="5cbce-119">Thus, you can be sure which object placed the error code in **Error.Number**, as well as which object originally generated the error (**Error.Source**).</span></span>

## <a name="example"></a><span data-ttu-id="5cbce-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5cbce-120">Example</span></span>

<span data-ttu-id="5cbce-121">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="5cbce-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
