---
title: ShowAllRecords-Makroaktion
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308645"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="2dae0-102">ShowAllRecords-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="2dae0-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="2dae0-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2dae0-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2dae0-104">Mit der **AnzeigenAlleDatensätze** -Aktion können Sie alle angewendeten Filter aus der aktiven Tabelle, dem abfrageergebnissatz oder dem Formular entfernen und alle Datensätze in der Tabelle oder im Resultset oder alle Datensätze in der zugrunde liegenden Tabelle oder Abfrage des Formulars anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2dae0-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="2dae0-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2dae0-105">Setting</span></span>

<span data-ttu-id="2dae0-106">Die **AnzeigenAlleDatensätze** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="2dae0-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dae0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dae0-107">Remarks</span></span>

<span data-ttu-id="2dae0-108">Mit dieser Aktion können Sie sicherstellen, dass alle Datensätze (einschließlich geänderter oder neuer Datensätze) für eine Tabelle, einen abfrageergebnissatz oder ein Formular angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2dae0-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="2dae0-109">Durch diese Aktion wird eine Neuabfrage der Datensätze für ein Formular oder ein Unterformular verursacht.</span><span class="sxs-lookup"><span data-stu-id="2dae0-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="2dae0-110">Sie können diese Aktion auch verwenden, um alle Filter zu entfernen, die mit der **ApplyFilter** -Aktion angewendet wurden, der Befehl **Filter** auf der Registerkarte **Start** oder das Argument **Filter Name** oder **Where Condition** der OpenForm-Aktion. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2dae0-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="2dae0-111">Diese Aktion hat dieselbe Wirkung wie das Klicken auf **Filter umschalten** auf der Registerkarte **Start** oder mit der rechten Maustaste auf das gefilterte Feld und das Klicken auf **Filter aus...** in der Formular-, Layout-oder Datenblattansicht.</span><span class="sxs-lookup"><span data-stu-id="2dae0-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="2dae0-112">Verwenden Sie die **AnzeigenAlleDatensätze** -Methode des **DoCmd** -Objekts, um die **ANZEIGENALLEDATENSÄTZE** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2dae0-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="2dae0-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2dae0-113">Example</span></span>

<span data-ttu-id="2dae0-114">**Anwenden eines Filters mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="2dae0-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="2dae0-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span><span class="sxs-lookup"><span data-stu-id="2dae0-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dae0-120">Bedingung</span><span class="sxs-lookup"><span data-stu-id="2dae0-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="2dae0-121">Aktion</span><span class="sxs-lookup"><span data-stu-id="2dae0-121">Action</span></span></p></th>
<th><p><span data-ttu-id="2dae0-122">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="2dae0-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="2dae0-123">Kommentar</span><span class="sxs-lookup"><span data-stu-id="2dae0-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dae0-124">[Company Name Filters] = 1</span><span class="sxs-lookup"><span data-stu-id="2dae0-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="2dae0-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="2dae0-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="2dae0-126"><strong>Bedingung</strong>: [Firmen Name] wie &quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="2dae0-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="2dae0-127">Filtern nach Firmen, deren Name mit A, À, Á, Â, Ã oder Ä beginnt.</span><span class="sxs-lookup"><span data-stu-id="2dae0-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dae0-128">[Company Name Filters] = 2</span><span class="sxs-lookup"><span data-stu-id="2dae0-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="2dae0-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="2dae0-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="2dae0-130"><strong>Bedingung</strong>: [Firmen Name] wie &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="2dae0-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="2dae0-131">Filtern nach Firmennamen, die mit B beginnen.</span><span class="sxs-lookup"><span data-stu-id="2dae0-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dae0-132">[Company Name Filters] = 3</span><span class="sxs-lookup"><span data-stu-id="2dae0-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="2dae0-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="2dae0-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="2dae0-134"><strong>Bedingung</strong>: [Firmen Name] wie &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="2dae0-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="2dae0-135">Filtern nach Firmennamen, die mit C oder Ç beginnen.</span><span class="sxs-lookup"><span data-stu-id="2dae0-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dae0-136">... Aktionszeilen für D bis Y haben dasselbe Format wie für A bis C ...</span><span class="sxs-lookup"><span data-stu-id="2dae0-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dae0-137">[Company Name Filters] = 26</span><span class="sxs-lookup"><span data-stu-id="2dae0-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="2dae0-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="2dae0-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="2dae0-139"><strong>Bedingung</strong>: [Firmen Name] wie &quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="2dae0-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="2dae0-140">Filtern nach Firmennamen, die mit ZÆØ oder Å beginnen.</span><span class="sxs-lookup"><span data-stu-id="2dae0-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dae0-141">[Company Name Filters] = 27</span><span class="sxs-lookup"><span data-stu-id="2dae0-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="2dae0-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="2dae0-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2dae0-143">Zeigt alle Datensätze an.</span><span class="sxs-lookup"><span data-stu-id="2dae0-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dae0-144">[RecordsetClone]. RecordCount &gt;0</span><span class="sxs-lookup"><span data-stu-id="2dae0-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="2dae0-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="2dae0-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="2dae0-146"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="2dae0-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="2dae0-147">Verschiebt den Fokus auf das Steuerelement Firma, wenn Datensätze für den ausgewählten Buchstaben zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dae0-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

