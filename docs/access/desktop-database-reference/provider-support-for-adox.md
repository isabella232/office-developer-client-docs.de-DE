---
title: Anbieterunterstützung für ADOX
TOCTitle: Provider Support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b19d30f9b243629874f7219c5b23af895540eaa9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881139"
---
# <a name="provider-support-for-adox"></a>Anbieterunterstützung für ADOX


**Betrifft**: Access 2013, Office 2013

Abhängig vom jeweiligen OLE DB-Datenprovider werden bestimmte ADOX-Features nicht unterstützt. ADOX wird vollständig mit dem [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt. Die nicht unterstützten Features bei Verwendung des [Microsoft OLE DB-Anbieters für SQL Server](microsoft-ole-db-provider-for-sql-server.md), des [Microsoft OLE DB-Anbieters für ODBC](microsoft-ole-db-provider-for-odbc.md) oder des [Microsoft OLE DB-Anbieters für Oracle](microsoft-ole-db-provider-for-oracle.md) werden im Folgenden aufgeführt. ADOX wird nicht von anderen Microsoft OLE DB-Anbietern unterstützt.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Microsoft OLE DB-Anbieter für SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objekt oder Auflistung</p></th>
<th><p>Verwendungseinschränkung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catalog</strong>-Objekt</p></td>
<td><p>Die <strong>Create</strong>-Methode wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong>-Auflistung</p></td>
<td><p>Eigenschaften verfügen vor der Objekterstellung über Lese-/Schreibzugriff und sind beim Verweisen auf ein bestehendes Objekt schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Views</strong>-Auflistung</p></td>
<td><p><strong>Views</strong> wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedures</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedure</strong>-Objekt</p></td>
<td><p>Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> -Auflistung</p></td>
<td><p><strong>Users</strong> wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> -Auflistung</p></td>
<td><p><strong>Groups</strong> wird nicht unterstützt.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB-Anbieter für ODBC

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objekt oder Auflistung</p></th>
<th><p>Verwendungseinschränkung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catalog</strong>-Objekt</p></td>
<td><p>Die <strong>Create</strong>-Methode wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.
 Eigenschaften verfügen vor der Objekterstellung über Lese-/Schreibzugriff und sind beim Verweisen auf ein bestehendes Objekt schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedures</strong>-Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure</strong>-Objekt</p></td>
<td><p>Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Indexes</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> -Auflistung</p></td>
<td><p><strong>Users</strong> wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> -Auflistung</p></td>
<td><p><strong>Groups</strong> wird nicht unterstützt.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB-Anbieter für Oracle

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objekt oder Auflistung</p></th>
<th><p>Verwendungseinschränkung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catalog</strong>-Objekt</p></td>
<td><p>Die <strong>Create</strong>-Methode wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.
 Eigenschaften verfügen vor der Objekterstellung über Lese-/Schreibzugriff und sind beim Verweisen auf ein bestehendes Objekt schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Views</strong>-Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong> -Objekt</p></td>
<td><p>Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedures</strong>-Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure</strong>-Objekt</p></td>
<td><p>Die  <strong>Command</strong>-Eigenschaft wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Indexes</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> -Auflistung</p></td>
<td><p>Die Methoden <strong>Append</strong> und <strong>Delete</strong> werden nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> -Auflistung</p></td>
<td><p><strong>Users</strong> wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> -Auflistung</p></td>
<td><p><strong>Groups</strong> wird nicht unterstützt.</p></td>
</tr>
</tbody>
</table>

