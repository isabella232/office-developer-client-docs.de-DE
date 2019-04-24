---
title: SetOrderBy-Makroaktion
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 86834cd8b6132e8939067c0e34037ca1b0ef8bad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314609"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="d2f87-102">SetOrderBy-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="d2f87-102">SetOrderBy macro action</span></span>


<span data-ttu-id="d2f87-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2f87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2f87-104">Mit der **FestlegenSortiertNach**-Aktion legen Sie fest, wie die Datensätze in einem Formular, einem Bericht, einer Tabelle oder einem Abfrageergebnis sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2f87-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="d2f87-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d2f87-105">Setting</span></span>

<span data-ttu-id="d2f87-106">Die **FestlegenSortiertNach**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2f87-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2f87-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="d2f87-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d2f87-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2f87-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2f87-109"><strong>Sortiert nach</strong></span><span class="sxs-lookup"><span data-stu-id="d2f87-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="d2f87-110">Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält.</span><span class="sxs-lookup"><span data-stu-id="d2f87-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2f87-111"><strong>Steuerelementname</strong></span><span class="sxs-lookup"><span data-stu-id="d2f87-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d2f87-p101">Wenn das Argument angegeben ist und es sich beim aktiven Objekt um ein Formular oder einen Bericht handelt, der Name des Steuerelements, das dem zu sortierenden Unterformular oder Unterbericht entspricht. Wenn das Argument leer ist und es sich beim aktiven Objekt um ein Formular oder einen Bericht handelt, wird das übergeordnete Formular bzw. der übergeordnete Bericht sortiert.</span><span class="sxs-lookup"><span data-stu-id="d2f87-p101">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted. If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d2f87-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2f87-114">Remarks</span></span>

<span data-ttu-id="d2f87-115">Beim Ausführen dieser Makroaktion wird die Sortierung auf die Tabelle, das Formular, den Bericht oder das Datenblatt (Abfrageergebnis) angewendet, das aktiv ist und den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="d2f87-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="d2f87-p102">Das Argument Sortiert nach bildet den Namen des Felds oder der Felder, nach dem oder denen Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). Die **SortiertNach** -Eigenschaft des aktiven Objekts wird verwendet, um einen Sortierwert zu speichern, den Sie später anwenden können. SortiertNach-Werte werden mit den Objekten gespeichert, in denen sie erstellt werden. Sie werden automatisch geladen, wenn das Objekt geöffnet wird, jedoch nicht automatisch angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2f87-p102">The Order By argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time. OrderBy values are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="d2f87-121">Wenn Sie das Argument Sortiert nach durch Eingeben eines oder mehrerer Feldnamen festlegen und anschließend das Makro ausführen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="d2f87-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="d2f87-p103">Wenn Sie Datensätze in absteigender Reihenfolge sortieren möchten, geben Sie am Ende des Argumentausdrucks „Sortiert nach" die Zeichenfolge „DESC" ein. Wenn Sie beispielsweise Kundendatensätze in absteigender Reihenfolge nach Kontaktnamen sortieren möchten, legen Sie das Argument „Sortiert nach" auf „Kontaktperson DESC" fest. Wenn Sie Namen in absteigender Reihenfolge nach Nachname und in aufsteigender Reihenfolge nach Vorname sortieren möchten, legen Sie das Argument „Sortiert nach" auf „Nachname DESC, Vorname ASC" fest.</span><span class="sxs-lookup"><span data-stu-id="d2f87-p103">To sort records in descending order, type DESC at the end of the Order By argument expression. For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC". To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

