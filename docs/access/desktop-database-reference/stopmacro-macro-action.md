---
title: StopMacro Macro Action
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a918fd128456450c21b5a36e74b7266df661cb75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474358"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="033c0-102">StopMacro Macro Action</span><span class="sxs-lookup"><span data-stu-id="033c0-102">StopMacro Macro Action</span></span>

<span data-ttu-id="033c0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="033c0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="033c0-104">Die **StoppMakro** -Aktion können Sie das derzeit ausgeführte Makro anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="033c0-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="033c0-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="033c0-105">Setting</span></span>

<span data-ttu-id="033c0-106">Die **StoppMakro** -Aktion verfügt nicht über keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="033c0-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="033c0-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="033c0-107">Remarks</span></span>

<span data-ttu-id="033c0-108">Normalerweise verwenden Sie diese Aktion, wenn eine Bedingung das Makro anzuhalten vornimmt.</span><span class="sxs-lookup"><span data-stu-id="033c0-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="033c0-109">Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="033c0-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="033c0-110">Wenn der Ausdruck auf **True** (– 1) ausgewertet wird, beendet Microsoft Access das Makro aus.</span><span class="sxs-lookup"><span data-stu-id="033c0-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="033c0-111">Beispielsweise können Sie ein Makro erstellen, das einem Formular mit der täglichen Summen Reihenfolge für das Datum in einem benutzerdefinierten Dialogfeld geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="033c0-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="033c0-112">Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement **Bestelldatum** im Dialogfeld ein gültiges Datum enthält.</span><span class="sxs-lookup"><span data-stu-id="033c0-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="033c0-113">Wenn dies nicht der Fall, die **Abfrageergebnis** -Aktion kann eine Fehlermeldung angezeigt, und die **StoppMakro** -Aktion kann das Makro beenden.</span><span class="sxs-lookup"><span data-stu-id="033c0-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="033c0-114">Wenn das Makro die Aktionen **Echo** oder **Warnmeldungen** zum Aktivieren von Echo oder die Anzeige von systemmeldungen aus verwendet, wird von die **StoppMakro** -Aktion automatisch wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="033c0-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="033c0-115">Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="033c0-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="033c0-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="033c0-116">Example</span></span>

<span data-ttu-id="033c0-117">Das folgende Makro veranschaulicht die Verwendung der **BeiFehler** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="033c0-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="033c0-118">In diesem Beispiel gibt die **BeiFehler** -Aktion an, dass Access führen Sie eine benutzerdefinierte Fehlerbehandlung Makro mit dem Namen Fehlerhandler, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="033c0-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="033c0-119">Wenn ein Fehler auftritt, wird das Untermakro CatchErrors aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="033c0-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="033c0-120">Wenn die Fehlernummer 2102 ist, eine bestimmte Nachricht wird angezeigt, und Ausführung von Makros wird unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="033c0-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="033c0-121">Andernfalls wird eine Meldung, die Beschreibung des Fehlers angezeigt und das Makro wird angehalten, damit Sie zusätzliche Hinweise zur Problembehandlung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="033c0-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="033c0-122">Das Fehlerhandler Makro zeigt eine Meldung angezeigt, die auf das **MacroError** -Objekt zum Anzeigen von Informationen zu dem Fehler verweist.</span><span class="sxs-lookup"><span data-stu-id="033c0-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="033c0-123">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="033c0-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
