---
title: RunSQL-Makroaktion
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704581"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="95078-102">RunSQL-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="95078-102">RunSQL macro action</span></span>

<span data-ttu-id="95078-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95078-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95078-104">Sie können die **AusführenSQL** -Aktion verwenden, eine Aktionsabfrage Zugriff mithilfe der entsprechenden SQL-Anweisung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="95078-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="95078-105">Sie können auch eine Datendefinitionsabfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="95078-105">You can also run a data-definition query.</span></span>

> [!NOTE]
> <span data-ttu-id="95078-106">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="95078-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="95078-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="95078-107">Setting</span></span>

<span data-ttu-id="95078-108">Die **AusführenSQL** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="95078-108">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95078-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="95078-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="95078-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95078-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95078-111"><strong>SQL-Anweisung</strong></span><span class="sxs-lookup"><span data-stu-id="95078-111"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="95078-p102">Die SQL-Anweisung für die Aktionsabfrage oder die Datendefinitionsabfrage, die Sie ausführen möchten. Die maximale Länge dieser Anweisung beträgt 255 Zeichen. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="95078-p102">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95078-115"><strong>Transaktion verwenden</strong></span><span class="sxs-lookup"><span data-stu-id="95078-115"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="95078-p103">Aktivieren Sie <strong>Ja</strong>, um diese Abfrage in eine Transaktion einzuschließen. Wählen Sie <strong>Nein</strong>, wenn Sie keine Transaktion verwenden möchten. Die Standardeinstellung ist <strong>Ja</strong>. Die Abfrage wird möglicherweise schneller ausgeführt, wenn Sie für dieses Argument <strong>Nein</strong> wählen.</span><span class="sxs-lookup"><span data-stu-id="95078-p103">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="95078-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95078-120">Remarks</span></span>

<span data-ttu-id="95078-p104">Sie können Aktionsabfragen verwenden, um Datensätze anzufügen, zu löschen und zu aktualisieren und um das Resultset einer Abfrage als neue Tabelle zu speichern. Sie können Datendefinitionsabfragen verwenden, um Tabellen oder Indizes zu erstellen, zu ändern und zu löschen. Sie können die **AusführenSQL** -Aktion verwenden, um diese Vorgänge direkt aus einem Makro heraus auszuführen, ohne gespeicherte Abfragen verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="95078-p104">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="95078-124">Wenn Sie eine SQL-Anweisung, die mehr als 255 Zeichen eingeben müssen, verwenden Sie die **RunSQL** -Methode des **DoCmd** -Objekts in einem Visual Basic für Applikationen (VBA) Modul stattdessen.</span><span class="sxs-lookup"><span data-stu-id="95078-124">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="95078-125">Sie können SQL-Anweisungen bis zu 32.768 Zeichen in VBA eingeben.</span><span class="sxs-lookup"><span data-stu-id="95078-125">You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="95078-p106">Access-Abfragen sind normalerweise SQL-Anweisungen, die beim Entwerfen einer Abfrage im Entwurfsbereich des Abfragefensters erstellt werden. Die folgende Tabelle enthält eine Liste der Access-Aktions- und Datendefinitionsabfragen sowie die entsprechenden SQL-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="95078-p106">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95078-128">Abfragetyp</span><span class="sxs-lookup"><span data-stu-id="95078-128">Query type</span></span></p></th>
<th><p><span data-ttu-id="95078-129">SQL-Anweisung</span><span class="sxs-lookup"><span data-stu-id="95078-129">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95078-130"><strong>Aktion</strong></span><span class="sxs-lookup"><span data-stu-id="95078-130"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95078-131">Anfügen</span><span class="sxs-lookup"><span data-stu-id="95078-131">Append</span></span></p></td>
<td><p><span data-ttu-id="95078-132">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="95078-132">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95078-133">Löschen</span><span class="sxs-lookup"><span data-stu-id="95078-133">Delete</span></span></p></td>
<td><p><span data-ttu-id="95078-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="95078-134">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95078-135">Tabellenerstellung</span><span class="sxs-lookup"><span data-stu-id="95078-135">Make-table</span></span></p></td>
<td><p><span data-ttu-id="95078-136">WÄHLEN SIE... IN</span><span class="sxs-lookup"><span data-stu-id="95078-136">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95078-137">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="95078-137">Update</span></span></p></td>
<td><p><span data-ttu-id="95078-138">UPDATE</span><span class="sxs-lookup"><span data-stu-id="95078-138">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95078-139"><strong>Datendefinition (SQL-spezifisch)</strong></span><span class="sxs-lookup"><span data-stu-id="95078-139"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95078-140">Erstellen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="95078-140">Create a table</span></span></p></td>
<td><p><span data-ttu-id="95078-141">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="95078-141">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95078-142">Ändern einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="95078-142">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="95078-143">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="95078-143">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95078-144">Löschen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="95078-144">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="95078-145">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="95078-145">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95078-146">Erstellen eines Indexes</span><span class="sxs-lookup"><span data-stu-id="95078-146">Create an index</span></span></p></td>
<td><p><span data-ttu-id="95078-147">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="95078-147">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95078-148">Löschen eines Indexes</span><span class="sxs-lookup"><span data-stu-id="95078-148">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="95078-149">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="95078-149">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="95078-150">Zum Ändern von Daten in einer anderen Datenbank können Sie auch eine IN-Klausel mit diesen Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="95078-150">You can also use an IN clause with these statements to modify data in another database.</span></span>

> [!NOTE]
> <span data-ttu-id="95078-p107">Um eine Auswahlabfrage oder Kreuztabellenabfrage in einem Makro auszuführen, verwenden Sie das Argument Ansicht der ÖffnenAbfrage-Aktion zum Öffnen einer vorhandenen Auswahlabfrage oder Kreuztabellenabfrage in der Datenblattansicht. Auf dieselbe Weise können Sie auch bereits vorhandene Aktionsabfragen und SQL-spezifische Abfragen ausführen.</span><span class="sxs-lookup"><span data-stu-id="95078-p107">To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span>
