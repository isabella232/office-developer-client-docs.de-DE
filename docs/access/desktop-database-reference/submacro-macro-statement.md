---
title: Untermakro-Makroanweisung
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b514d0896be25e11436cd7d7ac9f924fdf7eb3f1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924981"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="0bd9b-102">Untermakro-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="0bd9b-102">Submacro macro statement</span></span>

<span data-ttu-id="0bd9b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bd9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0bd9b-104">**Untermakro** -Anweisung wird ein separates Makro im Makro-Designer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="0bd9b-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="0bd9b-105">Setting</span></span>

<span data-ttu-id="0bd9b-106">Die **Untermakro** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bd9b-107">Argument</span><span class="sxs-lookup"><span data-stu-id="0bd9b-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="0bd9b-108">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="0bd9b-108">Required</span></span></p></th>
<th><p><span data-ttu-id="0bd9b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bd9b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bd9b-110">Name</span><span class="sxs-lookup"><span data-stu-id="0bd9b-110">Name</span></span></p></td>
<td><p><span data-ttu-id="0bd9b-111">Ja</span><span class="sxs-lookup"><span data-stu-id="0bd9b-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="0bd9b-112">Eine Zeichenfolge, die als Name des Makros angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="0bd9b-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0bd9b-113">Example</span></span>

<span data-ttu-id="0bd9b-114">Das folgende Makro veranschaulicht die Verwendung der **BeiFehler** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="0bd9b-115">In diesem Beispiel gibt die **BeiFehler** -Aktion an, dass Access führen Sie eine benutzerdefinierte Fehlerbehandlung Makro mit dem Namen Fehlerhandler, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="0bd9b-116">Wenn ein Fehler auftritt, wird das Untermakro CatchErrors aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="0bd9b-117">Wenn die Fehlernummer 2102 ist, eine bestimmte Nachricht wird angezeigt, und Ausführung von Makros wird unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="0bd9b-118">Andernfalls wird eine Meldung, die Beschreibung des Fehlers angezeigt und das Makro wird angehalten, damit Sie zusätzliche Hinweise zur Problembehandlung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="0bd9b-119">Das Fehlerhandler Makro zeigt eine Meldung angezeigt, die auf das **MacroError** -Objekt zum Anzeigen von Informationen zu dem Fehler verweist.</span><span class="sxs-lookup"><span data-stu-id="0bd9b-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="0bd9b-120">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0bd9b-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
