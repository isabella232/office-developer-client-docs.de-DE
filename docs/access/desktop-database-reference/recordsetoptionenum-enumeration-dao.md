---
title: RecordsetOptionEnum-Enumeration (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45d4b67eecc54f526c8a88296b48784468118e67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473102"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="c7f75-102">RecordsetOptionEnum-Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="c7f75-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="c7f75-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7f75-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c7f75-104">Verwenden Sie die **OpenRecordset** -Methode, um die Merkmale eines neuen **Recordset** -Objekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c7f75-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7f75-105">Name</span><span class="sxs-lookup"><span data-stu-id="c7f75-105">Name</span></span></p></th>
<th><p><span data-ttu-id="c7f75-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c7f75-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c7f75-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7f75-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7f75-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="c7f75-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="c7f75-109">8</span><span class="sxs-lookup"><span data-stu-id="c7f75-109">8</span></span></p></td>
<td><p><span data-ttu-id="c7f75-110">Damit können Benutzer neue Datensätze zum Dynaset hinzufügen, vorhandene Datensätze können von den Benutzern jedoch nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="c7f75-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7f75-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="c7f75-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="c7f75-112">32</span><span class="sxs-lookup"><span data-stu-id="c7f75-112">32</span></span></p></td>
<td><p><span data-ttu-id="c7f75-113">Wendet Aktualisierungen nur auf die Felder an, die keine Auswirkungen auf andere Datensätze im Dynaset haben (nur Dynaset- und Momentaufnahmetyp).</span><span class="sxs-lookup"><span data-stu-id="c7f75-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7f75-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="c7f75-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="c7f75-115">2</span><span class="sxs-lookup"><span data-stu-id="c7f75-115">2</span></span></p></td>
<td><p><span data-ttu-id="c7f75-116">Verhindert, dass andere Benutzer Recordset-Datensätze (nur Tabellentyp) lesen.</span><span class="sxs-lookup"><span data-stu-id="c7f75-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7f75-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="c7f75-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="c7f75-118">1</span><span class="sxs-lookup"><span data-stu-id="c7f75-118">1</span></span></p></td>
<td><p><span data-ttu-id="c7f75-119">Verhindert, dass andere Benutzer Recordset-Datensätze ändern.</span><span class="sxs-lookup"><span data-stu-id="c7f75-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7f75-120">Bei der Ausführung</span><span class="sxs-lookup"><span data-stu-id="c7f75-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="c7f75-121">2048</span><span class="sxs-lookup"><span data-stu-id="c7f75-121">2048</span></span></p></td>
<td><p><span data-ttu-id="c7f75-122">Führt die Abfrage aus, ohne zunächst die SQLPrepare ODBC-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7f75-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7f75-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="c7f75-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="c7f75-124">128</span><span class="sxs-lookup"><span data-stu-id="c7f75-124">128</span></span></p></td>
<td><p><span data-ttu-id="c7f75-125">Setzt die Aktualisierungen zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c7f75-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7f75-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="c7f75-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="c7f75-127">256</span><span class="sxs-lookup"><span data-stu-id="c7f75-127">256</span></span></p></td>
<td><p><span data-ttu-id="c7f75-128">Erstellt einen Vorwärtsbildlauf-Datensatzes des Typs Momentaufnahme (nur Momentaufnahmentyp).</span><span class="sxs-lookup"><span data-stu-id="c7f75-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7f75-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="c7f75-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="c7f75-130">16</span><span class="sxs-lookup"><span data-stu-id="c7f75-130">16</span></span></p></td>
<td><p><span data-ttu-id="c7f75-131">Wendet Aktualisierungen auf alle Dynaset-Felder an, sogar wenn andere Datensätze betroffen sind (nur Dynaset- und Momentaufnahmetyp).</span><span class="sxs-lookup"><span data-stu-id="c7f75-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7f75-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="c7f75-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="c7f75-133">4</span><span class="sxs-lookup"><span data-stu-id="c7f75-133">4</span></span></p></td>
<td><p><span data-ttu-id="c7f75-134">Öffnet den Datensatz schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c7f75-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7f75-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="c7f75-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="c7f75-136">1024</span><span class="sxs-lookup"><span data-stu-id="c7f75-136">1024</span></span></p></td>
<td><p><span data-ttu-id="c7f75-137">Führt die Abfrage asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="c7f75-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7f75-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="c7f75-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="c7f75-139">512</span><span class="sxs-lookup"><span data-stu-id="c7f75-139">512</span></span></p></td>
<td><p><span data-ttu-id="c7f75-140">Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Dynaset-Typ).</span><span class="sxs-lookup"><span data-stu-id="c7f75-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7f75-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="c7f75-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="c7f75-142">64</span><span class="sxs-lookup"><span data-stu-id="c7f75-142">64</span></span></p></td>
<td><p><span data-ttu-id="c7f75-143">Sendet eine SQL-Anweisung an eine ODBC-Datenbank (nur Momentaufnahmetyp).</span><span class="sxs-lookup"><span data-stu-id="c7f75-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

