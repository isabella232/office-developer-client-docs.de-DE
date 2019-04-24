---
title: Verwenden von ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access bietet drei Objektmodelle, die Sie bei der Erstellung, Wartung und Verwaltung Ihrer Access-Datenbanken und der dazugehörigen Daten mithilfe von Visual Basic verwenden können.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312740"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="e14b1-103">Verwenden von ADO (ActiveX Data Objects)</span><span class="sxs-lookup"><span data-stu-id="e14b1-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="e14b1-104">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e14b1-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e14b1-105">Microsoft Access bietet drei Objektmodelle, die Sie bei der Erstellung, Wartung und Verwaltung Ihrer Access-Datenbanken und der dazugehörigen Daten mithilfe von Visual Basic verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e14b1-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="e14b1-106">Microsoft ActiveX Data-Objekte (ADO)</span><span class="sxs-lookup"><span data-stu-id="e14b1-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="e14b1-107">ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e14b1-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="e14b1-108">Microsoft ADO extern für DDL und Sicherheit (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e14b1-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="e14b1-109">ADOX stellt die DDL-Objekte (Data Definition Language) bereit, die zum Erstellen einer neuen Datenbank und der enthaltenen Objekte zusätzlich zu den zum Verwalten der Sicherheit erforderlichen Objekten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e14b1-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="e14b1-110">Microsoft Jet-und Replication Objects 2,5-Bibliothek (JRO)</span><span class="sxs-lookup"><span data-stu-id="e14b1-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="e14b1-111">Da ADO-Objekte zusätzlich zu Microsoft Jet-Datenbanken für die Zusammenarbeit mit vielen Datenbanken entworfen wurden, wurde die Jet-Funktionalität in die JRO-Bibliothek aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="e14b1-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="e14b1-112">Die folgende Liste listet die von jedem der neuen Objektmodelle bereitgestellten Funktionen im Vergleich zu DAO auf.</span><span class="sxs-lookup"><span data-stu-id="e14b1-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="e14b1-113">Funktionalität</span><span class="sxs-lookup"><span data-stu-id="e14b1-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="e14b1-114">DAO</span><span class="sxs-lookup"><span data-stu-id="e14b1-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="e14b1-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="e14b1-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="e14b1-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="e14b1-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="e14b1-117">JRO</span><span class="sxs-lookup"><span data-stu-id="e14b1-117">JRO</span></span><br />
<span data-ttu-id="e14b1-118">(Nur MDBs)</span><span class="sxs-lookup"><span data-stu-id="e14b1-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-119">Erstellen Sie Recordsets.</span><span class="sxs-lookup"><span data-stu-id="e14b1-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-120">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-120">X</span></span></p></td>
<td><p><span data-ttu-id="e14b1-121">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-122">Bearbeiten von Starteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e14b1-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-123">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-123">X</span></span></p></td>
<td><p><span data-ttu-id="e14b1-124">X \* \*</span><span class="sxs-lookup"><span data-stu-id="e14b1-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-125">Unterstützung von ANSI92 SQL. \* \* \*</span><span class="sxs-lookup"><span data-stu-id="e14b1-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-126">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-126">X</span></span></p></td>
<td><p><span data-ttu-id="e14b1-127">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-128">Erstellen Sie Tabellen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-129">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-130">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-131">Erstellen Sie eine neue Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e14b1-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-132">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-133">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-134">Bearbeiten vorhandener Tabelleneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e14b1-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-135">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-136">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-137">Erstellen von Tabellenbeziehungen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-138">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-139">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-140">Bearbeiten von Sicherheitseinstellungen</span><span class="sxs-lookup"><span data-stu-id="e14b1-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-141">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-142">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-143">Unterstützung für das Komprimierungsattribut für Spaltendaten.</span><span class="sxs-lookup"><span data-stu-id="e14b1-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-144">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-145">Bearbeiten gespeicherter, einfacher SQL-Abfragen oder-Ansichten.</span><span class="sxs-lookup"><span data-stu-id="e14b1-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-146">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-147">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-148">Erstellen permanenter Abfragen, auf die nur über Code zugegriffen werden kann</span><span class="sxs-lookup"><span data-stu-id="e14b1-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-149">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-150">Erstellen von Abfragen, auf die über Datenbankcontainer/UI und Code zugegriffen werden kann</span><span class="sxs-lookup"><span data-stu-id="e14b1-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-151">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-152">Komprimieren/Codieren der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e14b1-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-153">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-154">X4</span><span class="sxs-lookup"><span data-stu-id="e14b1-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-155">Cache aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e14b1-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-156">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-157">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-158">Datenbank replizierbar machen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-159">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-160">X3</span><span class="sxs-lookup"><span data-stu-id="e14b1-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-161">Erstellen von Datenbankreplikaten</span><span class="sxs-lookup"><span data-stu-id="e14b1-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-162">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-163">X3</span><span class="sxs-lookup"><span data-stu-id="e14b1-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-164">Synchronisieren von Replikaten</span><span class="sxs-lookup"><span data-stu-id="e14b1-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-165">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e14b1-166">X3</span><span class="sxs-lookup"><span data-stu-id="e14b1-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-167">Bearbeiten von Datenbankeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e14b1-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-168">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14b1-169">Erstellen benutzerdefinierter Datenbankeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e14b1-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-170">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14b1-171">Tabellenspalteneigenschaften bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e14b1-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="e14b1-172">X</span><span class="sxs-lookup"><span data-stu-id="e14b1-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e14b1-p101">\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.</span><span class="sxs-lookup"><span data-stu-id="e14b1-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="e14b1-175">\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.</span><span class="sxs-lookup"><span data-stu-id="e14b1-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="e14b1-176">\*\*\*Obwohl das Access-Datenbankmodul einige ANSI 92 SQL unterstützt, ist es noch nicht vollständig ANSI92-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e14b1-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="e14b1-177">1 verwendet **Connection** -Objekt, um auf Datenbank zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="e14b1-178">2 verwendet das **catalog** -Objekt, um auf Datenbank zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="e14b1-179">3 verwendet das **Replica** -Objekt, um auf Datenbank zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="e14b1-180">4 verwendet das **JetEngine** -Objekt, um auf Datenbank zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e14b1-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="e14b1-181">Im Gegensatz zu DAO können ADO-und ADOX-Objekte die markierten Aktionen in anderen Datenbanken als Jet ausführen, sofern der Anbieter dieser Datenbanken diese Aktion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e14b1-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


