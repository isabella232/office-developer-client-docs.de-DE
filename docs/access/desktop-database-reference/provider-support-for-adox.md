---
title: Anbieterunterstützung für ADOX
TOCTitle: Provider Support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d55ae14d124bfad7f8abbfcf3d94398ea92d792
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475810"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="3c011-102">Anbieterunterstützung für ADOX</span><span class="sxs-lookup"><span data-stu-id="3c011-102">Provider Support for ADOX</span></span>


<span data-ttu-id="3c011-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c011-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c011-p101">Abhängig vom jeweiligen OLE DB-Datenprovider werden bestimmte ADOX-Features nicht unterstützt. ADOX wird vollständig mit dem [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt. Die nicht unterstützten Features bei Verwendung des [Microsoft OLE DB-Anbieters für SQL Server](microsoft-ole-db-provider-for-sql-server.md), des [Microsoft OLE DB-Anbieters für ODBC](microsoft-ole-db-provider-for-odbc.md) oder des [Microsoft OLE DB-Anbieters für Oracle](microsoft-ole-db-provider-for-oracle.md) werden im Folgenden aufgeführt. ADOX wird nicht von anderen Microsoft OLE DB-Anbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="3c011-108">Microsoft OLE DB-Anbieter für SQL Server</span><span class="sxs-lookup"><span data-stu-id="3c011-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c011-109">Objekt oder Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="3c011-110">Verwendungseinschränkung</span><span class="sxs-lookup"><span data-stu-id="3c011-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c011-111"><strong>Catalog</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-112">Die <strong>Create</strong>-Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-113"><strong>Tables</strong>-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-114">Eigenschaften verfügen vor der Objekterstellung über Lese-/Schreibzugriff und sind beim Verweisen auf ein bestehendes Objekt schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-115"><strong>Views</strong>-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-116"><strong>Views</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-117"><strong>Procedures</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-118">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-119"><strong>Procedure</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-120">Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-121"><strong>Keys</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-122">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-123"><strong>Users</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-124"><strong>Users</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-125"><strong>Groups</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-126"><strong>Groups</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="3c011-127">Microsoft OLE DB-Anbieter für ODBC</span><span class="sxs-lookup"><span data-stu-id="3c011-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c011-128">Objekt oder Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="3c011-129">Verwendungseinschränkung</span><span class="sxs-lookup"><span data-stu-id="3c011-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c011-130"><strong>Catalog</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-131">Die <strong>Create</strong>-Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-132"><strong>Tables</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-133">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.
</span><span class="sxs-lookup"><span data-stu-id="3c011-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="3c011-134">Eigenschaften verfügen vor der Objekterstellung über Lese-/Schreibzugriff und sind beim Verweisen auf ein bestehendes Objekt schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-135"><strong>Procedures</strong>-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-136">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-137"><strong>Procedure</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-138">Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-139"><strong>Indexes</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-140">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-141"><strong>Keys</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-142">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-143"><strong>Users</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-144"><strong>Users</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-145"><strong>Groups</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-146"><strong>Groups</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="3c011-147">Microsoft OLE DB-Anbieter für Oracle</span><span class="sxs-lookup"><span data-stu-id="3c011-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c011-148">Objekt oder Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="3c011-149">Verwendungseinschränkung</span><span class="sxs-lookup"><span data-stu-id="3c011-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c011-150"><strong>Catalog</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-151">Die <strong>Create</strong>-Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-152"><strong>Tables</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-153">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.
</span><span class="sxs-lookup"><span data-stu-id="3c011-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="3c011-154">Eigenschaften verfügen vor der Objekterstellung über Lese-/Schreibzugriff und sind beim Verweisen auf ein bestehendes Objekt schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-155"><strong>Views</strong>-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-156">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-157"><strong>View</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-158">Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-159"><strong>Procedures</strong>-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-160">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-161"><strong>Procedure</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c011-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3c011-162">Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-163"><strong>Indexes</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-164">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-165"><strong>Keys</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-166">Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c011-167"><strong>Users</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-168"><strong>Users</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c011-169"><strong>Groups</strong> -Auflistung</span><span class="sxs-lookup"><span data-stu-id="3c011-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="3c011-170"><strong>Groups</strong> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c011-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

