---
title: LockTypeEnum (Aufzählung) (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec7095df2f2f050171a45fe3639f179eab40e8e1
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943899"
---
# <a name="locktypeenum-enumeration-dao"></a>LockTypeEnum (Aufzählung) (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt die Art der Datensatzsperrung an, die beim Öffnen eines Datensatzes verwendet wird.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbOptimistic</p></td>
<td><p>3</p></td>
<td><p>Vollständige Parallelität basierend auf der Datensatz-ID. Der Cursor vergleicht die Datensatz-ID in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden.</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>Aktiviert vollständige Batchaktualisierungen (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>Vollständige Parallelität basierend auf Datensatzwerten. Der Cursor vergleicht Datenwerte in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden (nur ODBCDirect-Arbeitsbereiche).</p>

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>Eingeschränkte Parallelität. Der Cursor verwendet die niedrigste Sperrebene, mit der sichergestellt ist, dass der Datensatz aktualisiert werden kann.</p></td>
</tr>
</tbody>
</table>

