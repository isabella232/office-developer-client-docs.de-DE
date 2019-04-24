---
title: StopMacro-Makroaktion
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308498"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="2ae5b-102">StopMacro-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="2ae5b-102">StopMacro macro action</span></span>

<span data-ttu-id="2ae5b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ae5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ae5b-104">Sie können die **stopmakro** -Aktion verwenden, um das derzeit ausgeführte Makro zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="2ae5b-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2ae5b-105">Setting</span></span>

<span data-ttu-id="2ae5b-106">Die **stopmakro** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae5b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ae5b-107">Remarks</span></span>

<span data-ttu-id="2ae5b-108">Diese Aktion wird in der Regel verwendet, wenn eine Bedingung das Beenden des Makros erforderlich macht.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="2ae5b-109">Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="2ae5b-110">Wenn der Ausdruck **true** ergibt (– 1), beendet Microsoft Access das Makro.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="2ae5b-111">Sie können beispielsweise ein Makro erstellen, das ein Formular öffnet, in dem die Gesamtsummen für das in einem benutzerdefinierten Dialogfeld eingegebene Datum angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="2ae5b-112">Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement **Order Date** im Dialogfeld ein gültiges Datum enthält.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="2ae5b-113">Wenn dies nicht der Fall ist, kann die **MessageBox** -Aktion eine Fehlermeldung anzeigen, und die **stopmakro** -Aktion kann das Makro beenden.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="2ae5b-114">Wenn das Makro die Aktionen **Echo** oder **Warn** Meldungen zum Ausschalten von Echo oder der Anzeige von Systemnachrichten verwendet hat, werden Sie von der **stopmakro** -Aktion automatisch wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="2ae5b-115">Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="2ae5b-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2ae5b-116">Example</span></span>

<span data-ttu-id="2ae5b-117">The following macro demonstrates the use of the **OnError** action.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="2ae5b-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="2ae5b-119">Wenn ein Fehler auftritt, wird das CatchErrors-unter Makro aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="2ae5b-120">Wenn die Fehlernummer 2102 ist, wird eine bestimmte Meldung angezeigt, und die Ausführung des Makros wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="2ae5b-121">Andernfalls wird eine Meldung mit dem Fehler angezeigt, und das Makro wird angehalten, damit Sie zusätzliche Problembehandlung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="2ae5b-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span><span class="sxs-lookup"><span data-stu-id="2ae5b-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="2ae5b-123">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2ae5b-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
