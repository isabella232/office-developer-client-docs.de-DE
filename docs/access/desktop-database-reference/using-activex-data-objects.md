---
title: Verwenden von ActiveX Data Objects
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access enthält drei Objektmodelle, verwenden Sie bei der Erstellung, warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887509"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="fad77-103">Verwenden von ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="fad77-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="fad77-104">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fad77-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fad77-105">Microsoft Access enthält drei Objektmodelle, verwenden Sie bei der Erstellung, warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fad77-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="fad77-106">Microsoft ActiveX Data-Objekte (ADO)</span><span class="sxs-lookup"><span data-stu-id="fad77-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="fad77-107">ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fad77-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="fad77-108">Microsoft ADO Ext Sicherheit (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fad77-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="fad77-109">ADOX stellt die Datendefinitionssprache (Data Definition Language, DDL)-Objekte, die erforderlich sind, zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den zum Verwalten der Sicherheit bereit.</span><span class="sxs-lookup"><span data-stu-id="fad77-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="fad77-110">Microsoft Jet and Replication Objects 2.5-Bibliothek (JRO)</span><span class="sxs-lookup"><span data-stu-id="fad77-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="fad77-111">Da ADO-Objekte für die Arbeit mit vielen Datenbanken neben den Microsoft Jet-Datenbanken konzipiert wurden, wurde die Jet-spezifische Funktionalität in die JRO-Bibliothek verlagert.</span><span class="sxs-lookup"><span data-stu-id="fad77-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="fad77-112">Die folgende Liste listet die von jedem der neuen Objektmodelle bereitgestellten Funktionen im Vergleich zu DAO auf.</span><span class="sxs-lookup"><span data-stu-id="fad77-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="fad77-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="fad77-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="fad77-114">DAO</span><span class="sxs-lookup"><span data-stu-id="fad77-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="fad77-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="fad77-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="fad77-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="fad77-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="fad77-117">JRO</span><span class="sxs-lookup"><span data-stu-id="fad77-117">JRO</span></span><br />
<span data-ttu-id="fad77-118">(Nur MDBs)</span><span class="sxs-lookup"><span data-stu-id="fad77-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fad77-119">Erstellen von Datensatzgruppen.</span><span class="sxs-lookup"><span data-stu-id="fad77-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="fad77-120">X</span><span class="sxs-lookup"><span data-stu-id="fad77-120">X</span></span></p></td>
<td><p><span data-ttu-id="fad77-121">X</span><span class="sxs-lookup"><span data-stu-id="fad77-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-122">Bearbeiten von Starteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fad77-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="fad77-123">X</span><span class="sxs-lookup"><span data-stu-id="fad77-123">X</span></span></p></td>
<td><p><span data-ttu-id="fad77-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="fad77-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-125">Unterstützung von ANSI92 SQL.\* \*\*</span><span class="sxs-lookup"><span data-stu-id="fad77-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-126">X</span><span class="sxs-lookup"><span data-stu-id="fad77-126">X</span></span></p></td>
<td><p><span data-ttu-id="fad77-127">X</span><span class="sxs-lookup"><span data-stu-id="fad77-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-128">Erstellen von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="fad77-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="fad77-129">X</span><span class="sxs-lookup"><span data-stu-id="fad77-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-130">X</span><span class="sxs-lookup"><span data-stu-id="fad77-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-131">Erstellen Sie neue Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fad77-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="fad77-132">X</span><span class="sxs-lookup"><span data-stu-id="fad77-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-133">X\*</span><span class="sxs-lookup"><span data-stu-id="fad77-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-134">Bearbeiten Sie vorhandener Tabelleneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fad77-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="fad77-135">X</span><span class="sxs-lookup"><span data-stu-id="fad77-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-136">X</span><span class="sxs-lookup"><span data-stu-id="fad77-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-137">Erstellen von tabellenbeziehungen.</span><span class="sxs-lookup"><span data-stu-id="fad77-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="fad77-138">X</span><span class="sxs-lookup"><span data-stu-id="fad77-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-139">X\*</span><span class="sxs-lookup"><span data-stu-id="fad77-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-140">Bearbeiten von Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fad77-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="fad77-141">X</span><span class="sxs-lookup"><span data-stu-id="fad77-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-142">X\*</span><span class="sxs-lookup"><span data-stu-id="fad77-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-143">Unterstützung des Attributs Compression für Spaltendaten.</span><span class="sxs-lookup"><span data-stu-id="fad77-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-144">X</span><span class="sxs-lookup"><span data-stu-id="fad77-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-145">Bearbeiten Sie gespeicherter SQL-Standardabfragen oder-Ansichten.</span><span class="sxs-lookup"><span data-stu-id="fad77-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="fad77-146">X</span><span class="sxs-lookup"><span data-stu-id="fad77-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-147">X\*</span><span class="sxs-lookup"><span data-stu-id="fad77-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-148">Erstellen permanenter Abfragen, auf die nur über Code zugegriffen werden kann</span><span class="sxs-lookup"><span data-stu-id="fad77-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-149">X\*</span><span class="sxs-lookup"><span data-stu-id="fad77-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-150">Erstellen von Abfragen, auf die über Datenbankcontainer/UI und Code zugegriffen werden kann</span><span class="sxs-lookup"><span data-stu-id="fad77-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="fad77-151">X</span><span class="sxs-lookup"><span data-stu-id="fad77-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-152">Codieren Sie komprimieren/Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fad77-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="fad77-153">X</span><span class="sxs-lookup"><span data-stu-id="fad77-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-154">X4</span><span class="sxs-lookup"><span data-stu-id="fad77-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-155">Aktualisieren des Cachespeichers.</span><span class="sxs-lookup"><span data-stu-id="fad77-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="fad77-156">X</span><span class="sxs-lookup"><span data-stu-id="fad77-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-157">X</span><span class="sxs-lookup"><span data-stu-id="fad77-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-158">Machen Sie Datenbank replizierbar.</span><span class="sxs-lookup"><span data-stu-id="fad77-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="fad77-159">X</span><span class="sxs-lookup"><span data-stu-id="fad77-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-160">X3</span><span class="sxs-lookup"><span data-stu-id="fad77-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-161">Erstellen von Datenbankreplikaten.</span><span class="sxs-lookup"><span data-stu-id="fad77-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="fad77-162">X</span><span class="sxs-lookup"><span data-stu-id="fad77-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-163">X3</span><span class="sxs-lookup"><span data-stu-id="fad77-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-164">Synchronisieren von Replikaten.</span><span class="sxs-lookup"><span data-stu-id="fad77-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="fad77-165">X</span><span class="sxs-lookup"><span data-stu-id="fad77-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fad77-166">X3</span><span class="sxs-lookup"><span data-stu-id="fad77-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-167">Bearbeiten von Datenbankeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fad77-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="fad77-168">X</span><span class="sxs-lookup"><span data-stu-id="fad77-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fad77-169">Erstellen Sie benutzerdefinierter Datenbankeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fad77-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="fad77-170">X</span><span class="sxs-lookup"><span data-stu-id="fad77-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fad77-171">Bearbeiten von Tabellenspalteneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fad77-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="fad77-172">X</span><span class="sxs-lookup"><span data-stu-id="fad77-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fad77-p101">\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.</span><span class="sxs-lookup"><span data-stu-id="fad77-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="fad77-175">\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.</span><span class="sxs-lookup"><span data-stu-id="fad77-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="fad77-176">\*\*\*Obwohl das Access-Datenbankmodul ANSI 92 SQL unterstützt werden, ist es noch nicht vollständig ANSI92-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fad77-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="fad77-177">1 verwendet **Connection** -Objekts auf Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fad77-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="fad77-178">2 verwendet **Catalog** -Objekts auf Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fad77-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="fad77-179">3 verwendet **Replikat** -Objekts auf Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fad77-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="fad77-180">4 verwendet **JetEngine** -Objekts auf Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fad77-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="fad77-181">Im Gegensatz zu DAO können ADO- and ADOX-Objekte die gekennzeichneten Aktionen in Datenbanken als Jet ausführen, solange der Provider für diese Datenbanken die betreffende Aktion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fad77-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


