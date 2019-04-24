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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293833"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="17d0d-102">DisplayHourglassPointer-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="17d0d-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="17d0d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17d0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17d0d-p101">Mit der **AnzeigenSanduhrzeiger** -Aktion können Sie den Mauszeiger so ändern, dass er in Form einer Sanduhr (oder eines anderen Symbols, das Sie ausgewählt haben) angezeigt wird, während ein Makro ausgeführt wird. Diese Aktion bietet einen visuellen Hinweis darauf, dass ein Makro ausgeführt wird. Dies ist besonders nützlich, wenn die Ausführung einer Makroaktion oder des Makros selbst sehr viel Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="17d0d-p101">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="17d0d-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="17d0d-107">Setting</span></span>

<span data-ttu-id="17d0d-108">Die **AnzeigenSanduhrzeiger**-Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="17d0d-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17d0d-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="17d0d-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="17d0d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17d0d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17d0d-111"><strong>Sanduhr</strong></span><span class="sxs-lookup"><span data-stu-id="17d0d-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="17d0d-112">Klicken Sie im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator auf <strong>Ja</strong> (Symbol) oder <strong>Nein</strong> (zeigen Sie den normalen Mauszeiger) im Feld <strong>Sanduhr on</strong> im Bereich Action Arguments.</span><span class="sxs-lookup"><span data-stu-id="17d0d-112">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="17d0d-113">Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="17d0d-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="17d0d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17d0d-114">Remarks</span></span>

<span data-ttu-id="17d0d-115">Sie verwenden diese Aktion häufig, wenn Sie das Echo mithilfe der **Echo** -Aktion deaktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="17d0d-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="17d0d-116">Wenn Echo deaktiviert ist, werden die Bildschirmaktualisierungen von Access angehalten, bis das Makro abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="17d0d-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="17d0d-117">Access setzt das Argument **Sanduhr** automatisch auf **Nein** zurück, wenn die Makroausführung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="17d0d-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="17d0d-p104">In Microsoft Windows handelt es sich um das Symbol, das Sie für **Ausgelastet** im Dialogfeld **Eigenschaften von Maus** der Windows-Systemsteuerung festgelegt haben. Die Standardeinstellung für alle Windows-Betriebssysteme ist ein animiertes Sanduhrsymbol.</span><span class="sxs-lookup"><span data-stu-id="17d0d-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="17d0d-120">Wenn Sie möchten, können Sie ein anderes Symbol auswählen.</span><span class="sxs-lookup"><span data-stu-id="17d0d-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="17d0d-121">Verwenden Sie die **Hourglass** -Methode des **DoCmd** -Objekts, um die **AnzeigenSanduhrzeiger** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="17d0d-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

