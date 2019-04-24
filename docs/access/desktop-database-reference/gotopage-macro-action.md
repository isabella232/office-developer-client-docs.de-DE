---
title: GoToPage-Makroaktion
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 10d55b435a59594eaf3e8380b6690ebbda63a258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292160"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="ba92c-102">GoToPage-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="ba92c-102">GoToPage macro action</span></span>

<span data-ttu-id="ba92c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba92c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba92c-p101">Mit der **GeheZuSeite** -Aktion können Sie den Fokus im aktiven Formular auf das erste Steuerelement auf einer angegebenen Seite verschieben. Sie können diese Aktion verwenden, wenn Sie ein Formular mit Seitenumbrüchen erstellt haben, das Gruppen verwandter Informationen enthält. Sie könnten Sie z. B. ein Mitarbeiterformular verwenden, das persönliche Informationen auf der einen Seite, firmenbezogene Informationen auf einer weiteren Seite und Umsatzinformationen auf einer dritten Seite enthält. Mit der **GeheZuSeite** -Aktion können Sie den Fokus auf die gewünschte Seite verschieben. Sie können auch Registersteuerelemente verwenden, um mehrere Seiten mit Informationen auf einem einzigen Formular darzustellen.</span><span class="sxs-lookup"><span data-stu-id="ba92c-p101">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="ba92c-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ba92c-109">Setting</span></span>

<span data-ttu-id="ba92c-110">Die **GeheZuSeite**-Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="ba92c-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba92c-111">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="ba92c-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ba92c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba92c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba92c-113"><strong>Seitenzahl</strong></span><span class="sxs-lookup"><span data-stu-id="ba92c-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="ba92c-114">Die Nummer der Seite, auf die Sie den Fokus verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="ba92c-114">The number of the page to which you want to move the focus.</span></span> <span data-ttu-id="ba92c-115">Geben Sie die Seitenzahl im Feld <strong>Seitenzahl</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein.</span><span class="sxs-lookup"><span data-stu-id="ba92c-115">Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="ba92c-116">Wenn Sie dieses Argument nicht angeben, bleibt der Fokus auf der aktuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="ba92c-116">If you leave this argument blank, the focus stays on the current page.</span></span> <span data-ttu-id="ba92c-117">Sie können die Argumente <strong>right</strong> und <strong>down</strong> verwenden, um den Teil der Seite anzuzeigen, den Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba92c-117">You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba92c-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="ba92c-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="ba92c-p103">Die horizontale Ausrichtung der Stelle auf der Seite, gemessen vom linken Rand des umgebenden Fensters, die am linken Rand des Fensters angezeigt werden soll. Dieses Argument ist erforderlich, wenn Sie das Argument <strong>Abwärts</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="ba92c-p103">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window. This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba92c-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="ba92c-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="ba92c-p104">Die vertikale Ausrichtung der Stelle auf der Seite, gemessen vom oberen Rand des umgebenden Fensters, die am oberen Rand des Fensters angezeigt werden soll. Dieses Argument ist erforderlich, wenn Sie das Argument <strong>Rechts</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="ba92c-p104">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window. This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ba92c-124">Die Argumente **Rechts** und **Abwärts** werden, abhängig von den regionalen Einstellungen in der Windows-Systemsteuerung, in Zoll oder Zentimetern gemessen.</span><span class="sxs-lookup"><span data-stu-id="ba92c-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba92c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba92c-125">Remarks</span></span>

<span data-ttu-id="ba92c-p105">Sie können diese Aktion verwenden, um das erste Steuerelement (gemäß Definition in der Aktivierreihenfolge des Formulars) auf der angegebenen Seite auszuwählen. Verwenden Sie die **GeheZuSteuerelement**-Aktion, um den Fokus auf ein bestimmtes Steuerelement im Formular zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ba92c-p105">You can use this action to select the first control (as defined by the form's tab order) on the specified page. Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="ba92c-128">Sie können die Argumente **right** und **down** für Formulare mit Seiten größer als das Access-Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="ba92c-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="ba92c-129">Verwenden Sie das Argument **Seitenzahl**, um sich zur gewünschten Seite zu bewegen, und verwenden Sie dann die Argumente **Rechts** und **Abwärts**, um den gewünschten Teil der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba92c-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="ba92c-130">Access zeigt den Teil der Seite an, dessen obere linke Ecke den angegebenen Abstand von der linken oberen Ecke der Seite hat.</span><span class="sxs-lookup"><span data-stu-id="ba92c-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="ba92c-131">In den folgenden Fällen können Sie die **GeheZuSeite** -Aktion nicht verwenden:</span><span class="sxs-lookup"><span data-stu-id="ba92c-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="ba92c-132">Setzen des Fokus auf eine Seite eines ausgeblendeten Formulars.</span><span class="sxs-lookup"><span data-stu-id="ba92c-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="ba92c-133">Verschieben des Fokus von einer Seite zu einer anderen innerhalb des Registersteuerelements.</span><span class="sxs-lookup"><span data-stu-id="ba92c-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="ba92c-134">Verwenden Sie die **GoToPage** -Methode des **DoCmd** -Objekts, um die **GeheZuSeite** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ba92c-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

