---
title: Untermakro-Makroanweisung
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308470"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="c716d-102">Untermakro-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="c716d-102">Submacro macro statement</span></span>

<span data-ttu-id="c716d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c716d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c716d-104">Die **submacro** -Anweisung definiert ein separates Makro im Makro-Designer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="c716d-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="c716d-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c716d-105">Setting</span></span>

<span data-ttu-id="c716d-106">Die **Untermakro**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c716d-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c716d-107">Argument</span><span class="sxs-lookup"><span data-stu-id="c716d-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="c716d-108">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c716d-108">Required</span></span></p></th>
<th><p><span data-ttu-id="c716d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c716d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c716d-110">Name</span><span class="sxs-lookup"><span data-stu-id="c716d-110">Name</span></span></p></td>
<td><p><span data-ttu-id="c716d-111">Ja</span><span class="sxs-lookup"><span data-stu-id="c716d-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="c716d-112">Eine Zeichenfolge, die als Name des Makros angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c716d-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="c716d-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c716d-113">Example</span></span>

<span data-ttu-id="c716d-114">The following macro demonstrates the use of the **OnError** action.</span><span class="sxs-lookup"><span data-stu-id="c716d-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="c716d-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span><span class="sxs-lookup"><span data-stu-id="c716d-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="c716d-116">Wenn ein Fehler auftritt, wird das CatchErrors-unter Makro aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c716d-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="c716d-117">Wenn die Fehlernummer 2102 ist, wird eine bestimmte Meldung angezeigt, und die Ausführung des Makros wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="c716d-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="c716d-118">Andernfalls wird eine Meldung mit dem Fehler angezeigt, und das Makro wird angehalten, damit Sie zusätzliche Problembehandlung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="c716d-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="c716d-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span><span class="sxs-lookup"><span data-stu-id="c716d-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="c716d-120">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c716d-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
