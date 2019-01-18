---
title: OnError-Makroaktion
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711819"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="6855d-102">OnError-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="6855d-102">OnError macro action</span></span>

<span data-ttu-id="6855d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6855d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6855d-104">Mit der **BeiFehler** -Aktion können Sie angeben, was geschehen soll, wenn in einem Makro ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="6855d-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="6855d-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6855d-105">Setting</span></span>

<span data-ttu-id="6855d-106">Die **BeiFehler** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="6855d-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6855d-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="6855d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6855d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6855d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6855d-109">Gehe zu</span><span class="sxs-lookup"><span data-stu-id="6855d-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="6855d-p101">Geben Sie das allgemeine Verhalten an, das auftreten soll, wenn ein Fehler entdeckt wird. Klicken Sie auf den Dropdownpfeil, und klicken Sie dann auf eine der folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="6855d-p101">Specify the general behavior that should occur when an error is encountered. Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6855d-112">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6855d-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="6855d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6855d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6855d-114"><strong>Nächste</strong></span><span class="sxs-lookup"><span data-stu-id="6855d-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="6855d-p102">Microsoft Office Access 2007 zeichnet die Details des Fehlers im <strong>MacroError</strong>-Objekt auf, das Makro wird jedoch nicht beendet. Das Makro wird mit der nächsten Aktion fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6855d-p102">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro. The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6855d-117"><strong>Makroname</strong></span><span class="sxs-lookup"><span data-stu-id="6855d-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6855d-118">Access beendet das aktuelle Makro und führt das im Argument <strong>Makroname</strong> genannte Makro aus.</span><span class="sxs-lookup"><span data-stu-id="6855d-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6855d-119"><strong>Fail</strong></span><span class="sxs-lookup"><span data-stu-id="6855d-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="6855d-120">Access beendet das aktuelle Makro und zeigt eine Fehlermeldung an.</span><span class="sxs-lookup"><span data-stu-id="6855d-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6855d-121">Makroname</span><span class="sxs-lookup"><span data-stu-id="6855d-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="6855d-122">Wenn das Argument Gehe zu auf den Namen des Makros festgelegt ist, geben Sie den Namen des Makros zur Fehlerbehandlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6855d-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="6855d-123">Der eingegebene Name muss einen Namen in der Spalte <strong>Makroname den Namen</strong> des aktuellen Makros übereinstimmen; Sie können nicht den Namen eines anderen Makro-Objekts eingeben.</span><span class="sxs-lookup"><span data-stu-id="6855d-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="6855d-124">Im folgenden Beispiel wird das Makro <strong>Fehlerhandler</strong> in das gleiche Makroobjekt wie die <strong>BeiFehler</strong> -Aktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="6855d-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="6855d-125">Dieses Argument muss leer bleiben, wenn das Argument Gehe zu auf <strong>nächste</strong> oder <strong>Fehler</strong>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6855d-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6855d-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6855d-126">Remarks</span></span>

- <span data-ttu-id="6855d-p104">Die **BeiFehler** -Aktion wird gewöhnlich zu Beginn eines Makros platziert, sie kann jedoch auch später im Makro platziert werden. Die in der Aktion eingerichteten Regeln werden bei jedem Ausführen der Aktion wirksam.</span><span class="sxs-lookup"><span data-stu-id="6855d-p104">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro. The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="6855d-p105">Wenn Sie das Argument Gehe zu auf **Fehler** festlegen, verhält Access sich so, als befände sich keine **BeiFehler** -Aktion im Makro. Das heißt, wenn ein Fehler entdeckt wird, beendet Access das Makro, und es wird eine Standardfehlermeldung angezeigt. Die Hauptverwendung für die Einstellung **Fehler** besteht im Ausschalten jeder zuvor im Makro eingerichteten Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="6855d-p105">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro. That is, if an error is encountered, Access stops the macro and displays a standard error message. The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="6855d-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6855d-132">Example</span></span>

<span data-ttu-id="6855d-133">Das folgende Makro veranschaulicht die Verwendung der **BeiFehler** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="6855d-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="6855d-134">In diesem Beispiel gibt die **BeiFehler** -Aktion an, dass Access führen Sie eine benutzerdefinierte Fehlerbehandlung Makro mit dem Namen Fehlerhandler, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="6855d-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="6855d-135">Wenn ein Fehler auftritt, wird das Untermakro CatchErrors aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6855d-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="6855d-136">Wenn die Fehlernummer 2102 ist, eine bestimmte Nachricht wird angezeigt, und Ausführung von Makros wird unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="6855d-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="6855d-137">Andernfalls wird eine Meldung, die Beschreibung des Fehlers angezeigt und das Makro wird angehalten, damit Sie zusätzliche Hinweise zur Problembehandlung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="6855d-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="6855d-138">Das Fehlerhandler Makro zeigt eine Meldung angezeigt, die auf das **MacroError** -Objekt zum Anzeigen von Informationen zu dem Fehler verweist.</span><span class="sxs-lookup"><span data-stu-id="6855d-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="6855d-139">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6855d-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
