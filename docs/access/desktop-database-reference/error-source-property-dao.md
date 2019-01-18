---
title: Error.Source-Eigenschaft (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707409"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="eb51b-102">Error.Source-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb51b-102">Error.Source property (DAO)</span></span>


<span data-ttu-id="eb51b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb51b-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="eb51b-104">Gibt den Namen des Objekts zurück, das den Fehler ursprünglich erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="eb51b-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb51b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb51b-105">Syntax</span></span>

<span data-ttu-id="eb51b-106">*Ausdruck* . Quelle</span><span class="sxs-lookup"><span data-stu-id="eb51b-106">*expression* .Source</span></span>

<span data-ttu-id="eb51b-107">*expression* Eine Variable, die ein **Error**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb51b-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb51b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb51b-108">Remarks</span></span>

<span data-ttu-id="eb51b-p101">Der Wert der **Source**-Eigenschaft ist gewöhnlich der Klassenname oder die Programm-ID des Objekts. Mit der **Source**-Eigenschaft können Sie dem Benutzer Informationen darüber liefern, ob der Code Fehler behandeln kann, die von einem Objekt in einer anderen Anwendung erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="eb51b-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="eb51b-111">Angenommen, wenn Sie auf Microsoft Excel zugreifen und ein "Division durch Null"-Fehler generiert, Microsoft Excel legt **Error.Number** auf die Microsoft Excel-Code für diesen Fehler und die **Source** -Eigenschaft auf Excel.Application.</span><span class="sxs-lookup"><span data-stu-id="eb51b-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="eb51b-112">Beachten Sie, dass, wenn der Fehler in ein anderes Objekt von Microsoft Excel aufgerufen, generiert wird, wird Microsoft Excel den Fehler abfängt und **Error.Number** weiterhin auf die Microsoft Excel-Code festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb51b-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="eb51b-113">Die anderen **Fehler** Objekteigenschaften (einschließlich **Quelle**) behalten die Werte als Satz durch das Objekt jedoch, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="eb51b-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="eb51b-114">Die **Source** -Eigenschaft enthält immer den Namen des Objekts, das den Fehler ursprünglich erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="eb51b-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="eb51b-p103">Basierend auf der gesamten Fehlerdokumentation können Sie Code schreiben, der den Fehler angemessen behandelt. Wenn Ihre Fehlerbehandlung fehlschlägt, können Sie den Fehler mithilfe der Informationen des **[Error](error-object-dao.md)** -Objekts für den Benutzer beschreiben. Hierzu können Sie die **Source**-Eigenschaft und die anderen **Error**-Eigenschaften verwenden, um den Benutzer darüber zu informieren, welches Objekt den Fehler ursprünglich verursacht hat, eine Fehlerbeschreibung zu liefern usw.</span><span class="sxs-lookup"><span data-stu-id="eb51b-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <span data-ttu-id="eb51b-p104">Das **On Error Resume Next**-Konstrukt ist möglicherweise **On Error GoTo** vorzuziehen, wenn Fehler behandelt werden, die während des Zugriffs auf andere Objekte erzeugt wurden. Wenn das **Error**-Objekt nach jeder Interaktion mit einem Objekt überprüft wird, kann jeder Zweifel darüber aus dem Weg geräumt werden, auf welches Objekt der Code beim Auftreten des Fehlers zugegriffen hat. Auf diese Weise wissen Sie, welches Objekt den Fehlercode in **Error.Number** geschrieben und welches Objekt den Fehler ursprünglich erzeugt hat (**Error.Source**).</span><span class="sxs-lookup"><span data-stu-id="eb51b-p104">The **On Error Resume Next** construct may be preferable to **On Error GoTo** when dealing with errors generated during access to other objects. Checking the **Error** object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred. Thus, you can be sure which object placed the error code in **Error.Number**, as well as which object originally generated the error (**Error.Source**).</span></span>

## <a name="example"></a><span data-ttu-id="eb51b-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eb51b-120">Example</span></span>

<span data-ttu-id="eb51b-121">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="eb51b-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
