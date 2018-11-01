---
title: Untermakro-Makroanweisung
TOCTitle: Submacro Macro Statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de0d7066927e3a3cf034197c15f4330302801c0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885927"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="13699-102">Untermakro-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="13699-102">Submacro Macro Statement</span></span>

<span data-ttu-id="13699-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13699-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13699-104">Mit der **Untermakro** -Anweisung wird im Makro-Designer-Fenster ein separates Makro erstellt.</span><span class="sxs-lookup"><span data-stu-id="13699-104">The **Submacro** statement defines a seperate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="13699-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="13699-105">Setting</span></span>

<span data-ttu-id="13699-106">Die **Untermakro** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13699-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13699-107">Argument</span><span class="sxs-lookup"><span data-stu-id="13699-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="13699-108">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="13699-108">Required</span></span></p></th>
<th><p><span data-ttu-id="13699-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13699-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13699-110">Name</span><span class="sxs-lookup"><span data-stu-id="13699-110">Name</span></span></p></td>
<td><p><span data-ttu-id="13699-111">Ja</span><span class="sxs-lookup"><span data-stu-id="13699-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="13699-112">Eine Zeichenfolge, die als Name des Makros angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="13699-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="13699-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="13699-113">Example</span></span>

<span data-ttu-id="13699-114">Das folgende Makro veranschaulicht die Verwendung der **BeiFehler** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="13699-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="13699-115">In diesem Beispiel gibt die **BeiFehler** -Aktion an, dass Access führen Sie eine benutzerdefinierte Fehlerbehandlung Makro mit dem Namen Fehlerhandler, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="13699-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="13699-116">Wenn ein Fehler auftritt, wird das Untermakro CatchErrors aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="13699-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="13699-117">Wenn die Fehlernummer 2102 ist, eine bestimmte Nachricht wird angezeigt, und Ausführung von Makros wird unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="13699-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="13699-118">Andernfalls wird eine Meldung, die Beschreibung des Fehlers angezeigt und das Makro wird angehalten, damit Sie zusätzliche Hinweise zur Problembehandlung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="13699-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="13699-119">Das Fehlerhandler Makro zeigt eine Meldung angezeigt, die auf das **MacroError** -Objekt zum Anzeigen von Informationen zu dem Fehler verweist.</span><span class="sxs-lookup"><span data-stu-id="13699-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="13699-120">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="13699-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
