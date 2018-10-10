---
title: AusführenSQL-Makroaktion
TOCTitle: RunSQL Macro Action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ff4a363f6fbb05af582767f4b664f71f34d23357
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472697"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="f9862-102">AusführenSQL-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="f9862-102">RunSQL Macro Action</span></span>


<span data-ttu-id="f9862-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9862-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f9862-104">Sie können die **AusführenSQL** -Aktion verwenden, eine Aktionsabfrage Zugriff mithilfe der entsprechenden SQL-Anweisung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f9862-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="f9862-105">Sie können auch eine Datendefinitionsabfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9862-105">You can also run a data-definition query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f9862-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="f9862-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="f9862-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f9862-108">Setting</span></span>

<span data-ttu-id="f9862-109">Die **AusführenSQL** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f9862-109">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9862-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="f9862-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f9862-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9862-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9862-112"><strong>SQL-Anweisung</strong></span><span class="sxs-lookup"><span data-stu-id="f9862-112"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="f9862-p103">Die SQL-Anweisung für die Aktionsabfrage oder die Datendefinitionsabfrage, die Sie ausführen möchten. Die maximale Länge dieser Anweisung beträgt 255 Zeichen. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="f9862-p103">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-116"><strong>Transaktion verwenden</strong></span><span class="sxs-lookup"><span data-stu-id="f9862-116"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="f9862-p104">Aktivieren Sie <strong>Ja</strong>, um diese Abfrage in eine Transaktion einzuschließen. Wählen Sie <strong>Nein</strong>, wenn Sie keine Transaktion verwenden möchten. Die Standardeinstellung ist <strong>Ja</strong>. Die Abfrage wird möglicherweise schneller ausgeführt, wenn Sie für dieses Argument <strong>Nein</strong> wählen.</span><span class="sxs-lookup"><span data-stu-id="f9862-p104">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f9862-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f9862-121">Remarks</span></span>

<span data-ttu-id="f9862-p105">Sie können Aktionsabfragen verwenden, um Datensätze anzufügen, zu löschen und zu aktualisieren und um das Resultset einer Abfrage als neue Tabelle zu speichern. Sie können Datendefinitionsabfragen verwenden, um Tabellen oder Indizes zu erstellen, zu ändern und zu löschen. Sie können die **AusführenSQL** -Aktion verwenden, um diese Vorgänge direkt aus einem Makro heraus auszuführen, ohne gespeicherte Abfragen verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f9862-p105">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="f9862-125">Wenn Sie eine SQL-Anweisung, die mehr als 255 Zeichen eingeben müssen, verwenden Sie die **RunSQL** -Methode des **DoCmd** -Objekts in einem Visual Basic für Applikationen (VBA) Modul stattdessen.</span><span class="sxs-lookup"><span data-stu-id="f9862-125">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="f9862-126">Sie können SQL-Anweisungen bis zu 32.768 Zeichen in VBA eingeben.</span><span class="sxs-lookup"><span data-stu-id="f9862-126">You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="f9862-p107">Access-Abfragen sind normalerweise SQL-Anweisungen, die beim Entwerfen einer Abfrage im Entwurfsbereich des Abfragefensters erstellt werden. Die folgende Tabelle enthält eine Liste der Access-Aktions- und Datendefinitionsabfragen sowie die entsprechenden SQL-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f9862-p107">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9862-129">Abfragetyp</span><span class="sxs-lookup"><span data-stu-id="f9862-129">Query type</span></span></p></th>
<th><p><span data-ttu-id="f9862-130">SQL-Anweisung</span><span class="sxs-lookup"><span data-stu-id="f9862-130">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9862-131"><strong>Aktion</strong></span><span class="sxs-lookup"><span data-stu-id="f9862-131"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-132">Anfügen</span><span class="sxs-lookup"><span data-stu-id="f9862-132">Append</span></span></p></td>
<td><p><span data-ttu-id="f9862-133">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="f9862-133">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9862-134">Löschen</span><span class="sxs-lookup"><span data-stu-id="f9862-134">Delete</span></span></p></td>
<td><p><span data-ttu-id="f9862-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="f9862-135">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-136">Tabellenerstellung</span><span class="sxs-lookup"><span data-stu-id="f9862-136">Make-table</span></span></p></td>
<td><p><span data-ttu-id="f9862-137">WÄHLEN SIE... IN</span><span class="sxs-lookup"><span data-stu-id="f9862-137">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9862-138">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f9862-138">Update</span></span></p></td>
<td><p><span data-ttu-id="f9862-139">UPDATE</span><span class="sxs-lookup"><span data-stu-id="f9862-139">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-140"><strong>Datendefinition (SQL-spezifisch)</strong></span><span class="sxs-lookup"><span data-stu-id="f9862-140"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9862-141">Erstellen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="f9862-141">Create a table</span></span></p></td>
<td><p><span data-ttu-id="f9862-142">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="f9862-142">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-143">Ändern einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="f9862-143">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="f9862-144">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="f9862-144">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9862-145">Löschen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="f9862-145">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="f9862-146">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="f9862-146">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-147">Erstellen eines Indexes</span><span class="sxs-lookup"><span data-stu-id="f9862-147">Create an index</span></span></p></td>
<td><p><span data-ttu-id="f9862-148">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="f9862-148">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9862-149">Löschen eines Indexes</span><span class="sxs-lookup"><span data-stu-id="f9862-149">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="f9862-150">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="f9862-150">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f9862-151">Zum Ändern von Daten in einer anderen Datenbank können Sie auch eine IN-Klausel mit diesen Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9862-151">You can also use an IN clause with these statements to modify data in another database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f9862-p108">Um eine Auswahlabfrage oder Kreuztabellenabfrage in einem Makro auszuführen, verwenden Sie das Argument Ansicht der ÖffnenAbfrage-Aktion zum Öffnen einer vorhandenen Auswahlabfrage oder Kreuztabellenabfrage in der Datenblattansicht. Auf dieselbe Weise können Sie auch bereits vorhandene Aktionsabfragen und SQL-spezifische Abfragen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9862-p108">To run a select query or crosstab query from a macro, use the View argument of the <STRONG>OpenQuery</STRONG> action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span></P>


