---
title: ShowAllRecords Macro Action
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b6482bcd34562e13e1783f8e0702718eeaed0b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881734"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="54399-102">ShowAllRecords Macro Action</span><span class="sxs-lookup"><span data-stu-id="54399-102">ShowAllRecords Macro Action</span></span>


<span data-ttu-id="54399-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54399-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="54399-104">Sie können die **AnzeigenAlleDatensätze** -Aktion verwenden, um alle zugewiesenen Filter aus der aktiven Tabelle, Abfrage-Resultset oder Formular zu entfernen und alle Datensätze in der Tabelle oder des Resultsets oder alle Datensätze in des Formulars zugrunde liegenden Tabelle oder Abfrage anzeigen.</span><span class="sxs-lookup"><span data-stu-id="54399-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="54399-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="54399-105">Setting</span></span>

<span data-ttu-id="54399-106">Die **AnzeigenAlleDatensätze** -Aktion verfügt nicht über keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="54399-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="54399-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54399-107">Remarks</span></span>

<span data-ttu-id="54399-108">Sie können diese Aktion verwenden, um sicherzustellen, dass alle Datensätze (einschließlich aller veränderten oder neuen Datensätze) für eine Tabelle, Abfrage-Resultset oder Formular angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="54399-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="54399-109">Diese Aktion bewirkt, dass eine erneute Abfrage der Datensätze in einem Formular oder Unterformular.</span><span class="sxs-lookup"><span data-stu-id="54399-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="54399-110">Sie können diese Aktion auch verwenden, um alle Filter zu entfernen, der mit der **ApplyFilter** -Aktion, dem Befehl **Filter** auf der Registerkarte **Start** **Filternamen** oder der **Where-Bedingung** -Argument der **ÖffnenFormular** -Aktion angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="54399-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="54399-111">Diese Aktion hat dieselbe Wirkung wie das durch Klicken auf der Registerkarte **Start** auf **Filter ein/aus** oder mit der rechten Maustaste des gefilterten Felds und in der Formularansicht, Entwurfsansicht oder Datenblattansicht auf **Filter löschen aus** .</span><span class="sxs-lookup"><span data-stu-id="54399-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="54399-112">Führen Sie die **AnzeigenAlleDatensätze** -Aktion in einem Visual Basic für Applikationen (VBA) Modul mit **der ShowAllRecords** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="54399-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="54399-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="54399-113">Example</span></span>

<span data-ttu-id="54399-114">**Anwenden eines Filters mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="54399-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="54399-p102">Das folgende Makro enthält eine Reihe von Aktionen, die jeweils die Datensätze nach einem Formular Kunden-Telefonnummern filtern. Es zeigt die Verwendung der Aktionen AnwendenFilter, AnzeigenAlleDatensätze und GeheZuSteuerelement. Außerdem zeigt es die Verwendung von Bedingungen, mit denen ermittelt wird, welche Umschaltfläche in einer Optionsgruppe im Formular ausgewählt ist. Jeder Aktionszeile ist eine Umschaltfläche zugeordnet, mit der die mit A, B, C usw. beginnenden Datensatzgruppen oder alle Datensätze ausgewählt werden. Dieses Makro sollte dem AfterUpdate-Ereignis der Optionsgruppe CompanyNameFilter hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="54399-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54399-120">Bedingung</span><span class="sxs-lookup"><span data-stu-id="54399-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="54399-121">Aktion</span><span class="sxs-lookup"><span data-stu-id="54399-121">Action</span></span></p></th>
<th><p><span data-ttu-id="54399-122">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="54399-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="54399-123">Kommentar</span><span class="sxs-lookup"><span data-stu-id="54399-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54399-124">[Filter für Firma] = 1</span><span class="sxs-lookup"><span data-stu-id="54399-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="54399-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="54399-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="54399-126"><strong>Bedingung</strong>: [Firma] wie &quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="54399-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="54399-127">Filtern nach Firmen, deren Name mit A, À, Á, Â, Ã oder Ä beginnt.</span><span class="sxs-lookup"><span data-stu-id="54399-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54399-128">[Filter für Firma] = 2</span><span class="sxs-lookup"><span data-stu-id="54399-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="54399-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="54399-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="54399-130"><strong>Bedingung</strong>: [Firma] wie &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="54399-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="54399-131">Filtern nach Firmennamen, die mit B beginnen.</span><span class="sxs-lookup"><span data-stu-id="54399-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54399-132">[Filter für Firma] = 3</span><span class="sxs-lookup"><span data-stu-id="54399-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="54399-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="54399-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="54399-134"><strong>Bedingung</strong>: [Firma] wie &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="54399-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="54399-135">Filtern nach Firmennamen, die mit C oder Ç beginnen.</span><span class="sxs-lookup"><span data-stu-id="54399-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54399-136">... Aktionszeilen für D bis Y haben dasselbe Format wie für A bis C ...</span><span class="sxs-lookup"><span data-stu-id="54399-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54399-137">[Filter für Firma] = 26</span><span class="sxs-lookup"><span data-stu-id="54399-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="54399-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="54399-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="54399-139"><strong>Bedingung</strong>: [Firma] wie &quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="54399-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="54399-140">Filtern nach Firmennamen, die mit ZÆØ oder Å beginnen.</span><span class="sxs-lookup"><span data-stu-id="54399-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54399-141">[Filter für Firma] = 27</span><span class="sxs-lookup"><span data-stu-id="54399-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="54399-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="54399-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="54399-143">Zeigt alle Datensätze an.</span><span class="sxs-lookup"><span data-stu-id="54399-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54399-144">[RecordsetClone]. [RecordCount] &gt;0</span><span class="sxs-lookup"><span data-stu-id="54399-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="54399-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="54399-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="54399-146"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="54399-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="54399-147">Verschiebt den Fokus auf das Steuerelement Firma, wenn Datensätze für den ausgewählten Buchstaben zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54399-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

