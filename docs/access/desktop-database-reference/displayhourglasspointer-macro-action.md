---
title: DisplayHourglassPointer-Makroaktion
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a5635b2b97066394b8596dbcdb50c84abf429719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715130"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="2fcfe-102">DisplayHourglassPointer-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="2fcfe-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="2fcfe-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fcfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fcfe-p101">Mit der **AnzeigenSanduhrzeiger** -Aktion können Sie den Mauszeiger so ändern, dass er in Form einer Sanduhr (oder eines anderen Symbols, das Sie ausgewählt haben) angezeigt wird, während ein Makro ausgeführt wird. Diese Aktion bietet einen visuellen Hinweis darauf, dass ein Makro ausgeführt wird. Dies ist besonders nützlich, wenn die Ausführung einer Makroaktion oder des Makros selbst sehr viel Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-p101">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="2fcfe-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2fcfe-107">Setting</span></span>

<span data-ttu-id="2fcfe-108">Die **AnzeigenSanduhrzeiger** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fcfe-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="2fcfe-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2fcfe-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fcfe-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fcfe-111"><strong>Sanduhr</strong></span><span class="sxs-lookup"><span data-stu-id="2fcfe-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="2fcfe-p102">Klicken Sie im Feld Sanduhr des Abschnitts Aktionsargumente des Bereichs Makro-Generator auf Ja (Anzeige des Symbols) oder auf Nein (Anzeige des normalen Mauszeigers). Die Standardeinstellung ist Ja.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-p102">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2fcfe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fcfe-114">Remarks</span></span>

<span data-ttu-id="2fcfe-115">Sie verwenden diese Aktion häufig, wenn Sie das Echo mithilfe der **Echo** -Aktion deaktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="2fcfe-116">Wenn Echo deaktiviert ist, unterbricht Access Bildschirm Updates, bis das Makro beendet ist.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="2fcfe-117">Access setzt das Argument **Sanduhr** automatisch auf **Nein** zurück, wenn die Makroausführung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="2fcfe-p104">In Microsoft Windows handelt es sich um das Symbol, das Sie für **Ausgelastet** im Dialogfeld **Eigenschaften von Maus** der Windows-Systemsteuerung festgelegt haben. Die Standardeinstellung für alle Windows-Betriebssysteme ist ein animiertes Sanduhrsymbol.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="2fcfe-120">Wenn Sie möchten, können Sie ein anderes Symbol auswählen.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="2fcfe-121">Verwenden Sie die **Hourglass** -Methode des **DoCmd** -Objekts, um die **AnzeigenSanduhrzeiger** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2fcfe-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

