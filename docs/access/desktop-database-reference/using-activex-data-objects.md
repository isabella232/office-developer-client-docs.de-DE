---
title: Verwenden von ActiveX Data Objects (ADO)
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473774"
---
# <a name="using-activex-data-objects"></a><span data-ttu-id="40484-102">Verwenden von ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="40484-102">Using ActiveX Data Objects</span></span>


<span data-ttu-id="40484-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40484-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40484-104">Microsoft Access enthält drei Objektmodelle, die Sie beim Erstellen, Warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mit Visual Basic verwenden können.</span><span class="sxs-lookup"><span data-stu-id="40484-104">Microsoft Access provides three object models to use in the creation, maintaining and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="40484-105">Microsoft ActiveX Data-Objekte (ADO)</span><span class="sxs-lookup"><span data-stu-id="40484-105">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="40484-106">ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="40484-106">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="40484-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="40484-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span></span>

<span data-ttu-id="40484-108">ADOX stellt die DDL (Data Definition Language)-Objekte bereit, die zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den zum Verwalten der Zugriffsrechte benötigten Objekten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="40484-108">ADOX provides the Data Definition Language(DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

<span data-ttu-id="40484-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span><span class="sxs-lookup"><span data-stu-id="40484-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span></span>

<span data-ttu-id="40484-110">Da ADO-Objekte für die Zusammenarbeit mit vielen Datenbanken neben den Microsoft Jet-Datenbanken konzipiert wurden, wurde die Jet-spezifische Funktionalität in die JRO-Bibliothek verlagert.</span><span class="sxs-lookup"><span data-stu-id="40484-110">Since ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="40484-111">Die folgende Liste listet die von jedem der neuen Objektmodelle bereitgestellten Funktionen im Vergleich zu DAO auf.</span><span class="sxs-lookup"><span data-stu-id="40484-111">The following table lists the functionality provided by each compared to DAO.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40484-112">Funktion</span><span class="sxs-lookup"><span data-stu-id="40484-112">Functionality</span></span></p></th>
<th><p><span data-ttu-id="40484-113">DAO</span><span class="sxs-lookup"><span data-stu-id="40484-113">DAO</span></span></p></th>
<th><p><span data-ttu-id="40484-114">ADO1</span><span class="sxs-lookup"><span data-stu-id="40484-114">ADO1</span></span></p></th>
<th><p><span data-ttu-id="40484-115">ADOX2</span><span class="sxs-lookup"><span data-stu-id="40484-115">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="40484-116">JRO</span><span class="sxs-lookup"><span data-stu-id="40484-116">JRO</span></span><br />
<span data-ttu-id="40484-117">(Nur des MDB)</span><span class="sxs-lookup"><span data-stu-id="40484-117">(MDB's Only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40484-118">Erstellen von Datensatzgruppen</span><span class="sxs-lookup"><span data-stu-id="40484-118">Create Recordsets</span></span></p></td>
<td><p><span data-ttu-id="40484-119">X</span><span class="sxs-lookup"><span data-stu-id="40484-119">X</span></span></p></td>
<td><p><span data-ttu-id="40484-120">X</span><span class="sxs-lookup"><span data-stu-id="40484-120">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-121">Bearbeiten von Starteigenschaften</span><span class="sxs-lookup"><span data-stu-id="40484-121">Edit Startup properties</span></span></p></td>
<td><p><span data-ttu-id="40484-122">X</span><span class="sxs-lookup"><span data-stu-id="40484-122">X</span></span></p></td>
<td><p><span data-ttu-id="40484-123">X\*\*</span><span class="sxs-lookup"><span data-stu-id="40484-123">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-124">Unterstützung von ANSI92 SQL\*\*\*</span><span class="sxs-lookup"><span data-stu-id="40484-124">Support ANSI92 SQL\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-125">X</span><span class="sxs-lookup"><span data-stu-id="40484-125">X</span></span></p></td>
<td><p><span data-ttu-id="40484-126">X</span><span class="sxs-lookup"><span data-stu-id="40484-126">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-127">Erstellen von Tabellen</span><span class="sxs-lookup"><span data-stu-id="40484-127">Create Tables</span></span></p></td>
<td><p><span data-ttu-id="40484-128">X</span><span class="sxs-lookup"><span data-stu-id="40484-128">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-129">X</span><span class="sxs-lookup"><span data-stu-id="40484-129">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-130">Erstellen einer neuen Datenbank</span><span class="sxs-lookup"><span data-stu-id="40484-130">Create New Database</span></span></p></td>
<td><p><span data-ttu-id="40484-131">X</span><span class="sxs-lookup"><span data-stu-id="40484-131">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-132">X\*</span><span class="sxs-lookup"><span data-stu-id="40484-132">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-133">Bearbeiten vorhandener Tabelleneigenschaften</span><span class="sxs-lookup"><span data-stu-id="40484-133">Edit Existing Table properties</span></span></p></td>
<td><p><span data-ttu-id="40484-134">X</span><span class="sxs-lookup"><span data-stu-id="40484-134">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-135">X</span><span class="sxs-lookup"><span data-stu-id="40484-135">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-136">Erstellen von Tabellenbeziehungen</span><span class="sxs-lookup"><span data-stu-id="40484-136">Create table relationships</span></span></p></td>
<td><p><span data-ttu-id="40484-137">X</span><span class="sxs-lookup"><span data-stu-id="40484-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-138">X\*</span><span class="sxs-lookup"><span data-stu-id="40484-138">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-139">Bearbeiten von Sicherheitseinstellungen</span><span class="sxs-lookup"><span data-stu-id="40484-139">Edit security settings</span></span></p></td>
<td><p><span data-ttu-id="40484-140">X</span><span class="sxs-lookup"><span data-stu-id="40484-140">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-141">X\*</span><span class="sxs-lookup"><span data-stu-id="40484-141">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-142">Unterstützung des Attributs Compression für Spaltendaten</span><span class="sxs-lookup"><span data-stu-id="40484-142">Support for Compression attribute for column data</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-143">X</span><span class="sxs-lookup"><span data-stu-id="40484-143">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-144">Bearbeiten gespeicherter SQL-Standardabfragen oder -ansichten</span><span class="sxs-lookup"><span data-stu-id="40484-144">Edit stored, basic SQL queries or views</span></span></p></td>
<td><p><span data-ttu-id="40484-145">X</span><span class="sxs-lookup"><span data-stu-id="40484-145">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-146">X\*</span><span class="sxs-lookup"><span data-stu-id="40484-146">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-147">Erstellen permanenter Abfragen, auf die nur über Code zugegriffen werden kann</span><span class="sxs-lookup"><span data-stu-id="40484-147">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-148">X\*</span><span class="sxs-lookup"><span data-stu-id="40484-148">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-149">Erstellen von Abfragen, auf die über Datenbankcontainer/UI und Code zugegriffen werden kann</span><span class="sxs-lookup"><span data-stu-id="40484-149">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="40484-150">X</span><span class="sxs-lookup"><span data-stu-id="40484-150">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-151">Komprimieren/Verschlüsseln von Datenbanken</span><span class="sxs-lookup"><span data-stu-id="40484-151">Compact/Encode database</span></span></p></td>
<td><p><span data-ttu-id="40484-152">X</span><span class="sxs-lookup"><span data-stu-id="40484-152">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-153">X4</span><span class="sxs-lookup"><span data-stu-id="40484-153">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-154">Aktualisieren des Cachespeichers</span><span class="sxs-lookup"><span data-stu-id="40484-154">Refresh Cache</span></span></p></td>
<td><p><span data-ttu-id="40484-155">X</span><span class="sxs-lookup"><span data-stu-id="40484-155">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-156">X</span><span class="sxs-lookup"><span data-stu-id="40484-156">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-157">Datenbank replizierbar machen</span><span class="sxs-lookup"><span data-stu-id="40484-157">Make Database Replicable</span></span></p></td>
<td><p><span data-ttu-id="40484-158">X</span><span class="sxs-lookup"><span data-stu-id="40484-158">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-159">X3</span><span class="sxs-lookup"><span data-stu-id="40484-159">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-160">Erstellen von Datenbankreplikaten</span><span class="sxs-lookup"><span data-stu-id="40484-160">Make Database Replicas</span></span></p></td>
<td><p><span data-ttu-id="40484-161">X</span><span class="sxs-lookup"><span data-stu-id="40484-161">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-162">X3</span><span class="sxs-lookup"><span data-stu-id="40484-162">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-163">Synchronisieren von Replikaten</span><span class="sxs-lookup"><span data-stu-id="40484-163">Synchronize Replicas</span></span></p></td>
<td><p><span data-ttu-id="40484-164">X</span><span class="sxs-lookup"><span data-stu-id="40484-164">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="40484-165">X3</span><span class="sxs-lookup"><span data-stu-id="40484-165">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-166">Bearbeiten von Datenbankeigenschaften</span><span class="sxs-lookup"><span data-stu-id="40484-166">Edit Database properties</span></span></p></td>
<td><p><span data-ttu-id="40484-167">X</span><span class="sxs-lookup"><span data-stu-id="40484-167">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40484-168">Erstellen benutzerdefinierter Datenbankeigenschaften</span><span class="sxs-lookup"><span data-stu-id="40484-168">Create custom database properties</span></span></p></td>
<td><p><span data-ttu-id="40484-169">X</span><span class="sxs-lookup"><span data-stu-id="40484-169">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40484-170">Bearbeiten von Tabellenspalteneigenschaften</span><span class="sxs-lookup"><span data-stu-id="40484-170">Edit table column properties</span></span></p></td>
<td><p><span data-ttu-id="40484-171">X</span><span class="sxs-lookup"><span data-stu-id="40484-171">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40484-p101">\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.</span><span class="sxs-lookup"><span data-stu-id="40484-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="40484-174">\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.</span><span class="sxs-lookup"><span data-stu-id="40484-174">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="40484-175">\*\*\* Obwohl das Access-Datenbankmodul ANSI 92 SQL teilweise unterstützt, ist es noch nicht vollständig ANSI92-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="40484-175">\*\*\* Though the Access database engine does support some ANSI 92 SQL it is not yet fully ANSI92 compliant.</span></span>

<span data-ttu-id="40484-176">1Verweist mithilfe des **Connection** -Objekts auf Datenbank</span><span class="sxs-lookup"><span data-stu-id="40484-176">1 Uses **Connection** object to reference to database</span></span>

<span data-ttu-id="40484-177">2Verweist mithilfe des **Catalog** -Objekts auf Datenbank</span><span class="sxs-lookup"><span data-stu-id="40484-177">2 Uses **Catalog** object to reference database</span></span>

<span data-ttu-id="40484-178">3Verweist mithilfe des **Replica** -Objekts auf Datenbank</span><span class="sxs-lookup"><span data-stu-id="40484-178">3 Uses **Replica** object to reference database</span></span>

<span data-ttu-id="40484-179">4Verweist mithilfe des **JetEngine** -Objekts auf Datenbank</span><span class="sxs-lookup"><span data-stu-id="40484-179">4 Uses **JetEngine** object to reference database</span></span>


> [!NOTE]
> <P><span data-ttu-id="40484-180">[!HINWEIS] Im Gegensatz zu DAO können ADO- and ADOX-Objekte die gekennzeichneten Aktionen in anderen Datenbanken als Jet-Datenbanken ausführen, sofern der Provider für diese Datenbanken die betreffende Aktion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40484-180">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other then Jet as long as the provider for those databases supports that action.</span></span></P>


