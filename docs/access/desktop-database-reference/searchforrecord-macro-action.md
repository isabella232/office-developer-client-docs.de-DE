---
title: SearchForRecord-Makroaktion
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: efa763a77250e1d5c617358f31421804c772468b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702110"
---
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="f3037-102">SearchForRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="f3037-102">SearchForRecord macro action</span></span>


<span data-ttu-id="f3037-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3037-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3037-104">Sie können die **SuchenNachDatensatz** -Aktion verwenden, um nach einem bestimmten Datensatz in einer Tabelle, einer Abfrage, einem Formular oder einem Bericht zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f3037-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="f3037-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f3037-105">Setting</span></span>

<span data-ttu-id="f3037-106">Die **SuchenNachDatensatz** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f3037-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3037-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="f3037-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f3037-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3037-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3037-109"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-p101">Geben Sie den Datenbankobjekttyp ein, in dem Sie suchen, oder wählen Sie ihn aus. Sie können <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong> oder <strong>Bericht</strong> auswählen.</span><span class="sxs-lookup"><span data-stu-id="f3037-p101">Enter or select the type of database object that you are searching in. You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3037-112"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-p102">Geben Sie das Objekt ein, das den zu suchenden Datensatz enthält, oder wählen Sie es aus. In der Dropdownliste werden alle Datenbankobjekte angezeigt, die den durch das Argument <strong>Objekttyp</strong> ausgewählten Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f3037-p102">Enter or select the specific object that contains the record to search for. The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3037-115"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-116">Geben Sie den Ausgangspunkt und die Richtung für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="f3037-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3037-117">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f3037-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="f3037-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3037-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3037-119"><strong>Vorherige</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-120">Sucht vom aktuellen Datensatz ausgehend rückwärts.</span><span class="sxs-lookup"><span data-stu-id="f3037-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3037-121"><strong>Nächste</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-122">Sucht vom aktuellen Datensatz ausgehend vorwärts.</span><span class="sxs-lookup"><span data-stu-id="f3037-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3037-123"><strong>Erster</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-p103">Sucht vom ersten Datensatz ausgehend vorwärts. Das ist der Standardwert für dieses Argument.</span><span class="sxs-lookup"><span data-stu-id="f3037-p103">Search forward from the first record. This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3037-126"><strong>Letzter</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-127">Sucht vom letzten Datensatz ausgehend rückwärts.</span><span class="sxs-lookup"><span data-stu-id="f3037-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3037-128"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-129">Geben Sie die Kriterien für die Suche mit derselben Syntax wie eine SQL WHERE-Klausel ohne das Wort nur &quot;, in dem&quot;.</span><span class="sxs-lookup"><span data-stu-id="f3037-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="f3037-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f3037-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="f3037-131">Um ein Kriterium erstellen, die einen Wert aus einem Textfeld auf einem Formular enthält, müssen Sie einen Ausdruck erstellen, der mit dem Namen des Textfelds mit dem Wert für die Suche den ersten Teil der Kriterien verkettet.</span><span class="sxs-lookup"><span data-stu-id="f3037-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="f3037-132">Das folgende Kriterium wird beispielsweise das Feld Beschreibung für den Wert in das Textfeld mit dem Namen auf dem Formular mit dem Namen FrmCategories TxtDescription gesucht.</span><span class="sxs-lookup"><span data-stu-id="f3037-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="f3037-133">Ein Gleichheitszeichen (<strong>=</strong>) am Anfang des Ausdrucks und die Verwendung von Hochkommas (<strong>'</strong>) auf beiden Seiten des Verweises im Feld Text:</span><span class="sxs-lookup"><span data-stu-id="f3037-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f3037-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3037-134">Remarks</span></span>

- <span data-ttu-id="f3037-135">Falls mehrere Datensätze mit den Kriterien im Argument **Bedingung** übereinstimmen, legen die folgenden Einstellungen fest, welcher Datensatz gefunden wird:</span><span class="sxs-lookup"><span data-stu-id="f3037-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="f3037-136">**Der Datensatz argumenteinstellung** Finden Sie in der Tabelle im Abschnitt Einstellungen für Weitere Informationen zum Argument **Datensatz** .</span><span class="sxs-lookup"><span data-stu-id="f3037-136">**The Record argument setting**See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="f3037-137">**Die Sortierreihenfolge der Datensätze** Angenommen, wenn das Argument **Datensatz** auf der **ersten**festgelegt ist, kann die Sortierreihenfolge der Datensätze ändern welcher Datensatz gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f3037-137">**The sort order of the records**For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="f3037-p106">Das im Argument **Objektname** angegebene Argument muss vor dem Ausführen dieser Aktion geöffnet werden. Sonst treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f3037-p106">The object specified in the **Object Name** argument must be open before this action is run. Otherwise, an error occurs.</span></span>

- <span data-ttu-id="f3037-140">Werden die Kriterien im Argument **Bedingung** nicht gefunden, tritt kein Fehler auf, und der Fokus verbleibt auf dem aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f3037-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="f3037-p107">Bei der Suche nach dem vorherigen oder nächsten Datensatz findet kein "Umbruch" statt, wenn das Ende der Daten erreicht wird. Sind keine weiteren Datensätze vorhanden, die den Kriterien entsprechen, tritt kein Fehler auf, und der Fokus verbleibt auf dem aktuellen Datensatz. Wenn Sie bestätigen möchten, dass eine Übereinstimmung gefunden wurde, können Sie eine Bedingung für die nächste Aktion eingeben und festlegen, dass die Bedingung den im Argument **Bedingung** angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="f3037-p107">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data. If there are no further records that match the criteria, no error occurs and the focus remains on the current record. To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="f3037-144">Verwenden Sie die **SuchenNachDatensatz** -Methode des **DoCmd** -Objekts, um die **SuchenNachDatensatz** -Aktion in einem VBA-Modul auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f3037-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="f3037-p108">Die **SuchenNachDatensatz** -Aktion ähnelt der **[SuchenDatensatz](findrecord-macro-action.md)** -Aktion, allerdings verfügt **SuchenNachDatensatz** über leistungsfähigere Suchfunktionen. Die **SuchenDatensatz** -Aktion wird hauptsächlich für die Suche nach Zeichenfolgen verwendet und dupliziert die Funktionen des Dialogfelds **Suchen**. Die Kriterien der **SuchenNachDatensatz** -Aktion entsprechen dagegen eher einem Filter oder einer SQL-Abfrage. Die folgende Liste bietet Verwendungsbeispiele für die **SuchenNachDatensatz** -Aktion:</span><span class="sxs-lookup"><span data-stu-id="f3037-p108">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features. The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box. The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query. The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="f3037-149">Sie können komplexe Kriterien im Argument **Bedingung** verwenden, z. B.</span><span class="sxs-lookup"><span data-stu-id="f3037-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="f3037-150">Sie können auf Felder verweisen, die zwar in der Datensatzquelle eines Formulars oder Berichts angezeigt werden, nicht aber im Formular oder Bericht.</span><span class="sxs-lookup"><span data-stu-id="f3037-150">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report.</span></span> <span data-ttu-id="f3037-151">Im vorstehenden Beispiel muss Beschreibung weder CategoryID auf das Formular oder der Bericht für die Kriterien funktionieren angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3037-151">In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="f3037-p110">Sie können logische Operatoren verwenden, z. B. **\<**, **\>**, **AND**, **OR** und **BETWEEN**. Mit der **SuchenDatensatz** -Aktion werden nur Zeichenfolgen gefunden, die der gesuchten Zeichenfolge entsprechen, mit dieser beginnen oder sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3037-p110">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**. The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="f3037-154">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3037-154">Example</span></span>

<span data-ttu-id="f3037-p111">Mit dem folgenden Makro wird durch Verwendung der ÖffnenTabelle-Aktion zuerst die Tabelle Kategorien geöffnet. Anschließend sucht das Makro mithilfe der SuchenNachDatensatz-Aktion nach dem ersten Datensatz in der Tabelle, dessen Feld Description dem Wert "Getränke" entspricht.</span><span class="sxs-lookup"><span data-stu-id="f3037-p111">The following macro first opens the Categories table by using the **OpenTable** action. The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3037-157">Aktion</span><span class="sxs-lookup"><span data-stu-id="f3037-157">Action</span></span></p></th>
<th><p><span data-ttu-id="f3037-158">Argumente</span><span class="sxs-lookup"><span data-stu-id="f3037-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3037-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-160"><strong>Tabellenname</strong>: Kategorien<strong>Anzeigen</strong>: <strong>DatasheetData Modus</strong>: <strong>Bearbeiten</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3037-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="f3037-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="f3037-162"><strong>Objekttyp</strong>: <strong>TableObject Name</strong>: Kategorien<strong>Record</strong>: <strong>FirstWhere Bedingung</strong>: Description = &quot;Getränke&quot;</span><span class="sxs-lookup"><span data-stu-id="f3037-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

