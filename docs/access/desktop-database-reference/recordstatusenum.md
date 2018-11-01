---
title: RecordStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: fbff4e9ac28b1c5831131183203dd0d975bfb525
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868973"
---
# <a name="recordstatusenum"></a>RecordStatusEnum

**Betrifft**: Access 2013, Office 2013

Gibt den Status eines Datensatzes in Bezug auf Batchaktualisierungen und andere Mengenoperationen an.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adRecCanceled</strong></p></td>
<td><p>0 x 100</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da die Operation abgebrochen wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecCantRelease</strong></p></td>
<td><p>0 x 400</p></td>
<td><p>Gibt an, dass der neue Datensatz nicht gespeichert wurde, weil der vorhandene Datensatz gesperrt war.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecConcurrencyViolation</strong></p></td>
<td><p>0 x 800</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da eine vollständiger Parallelität verwendet wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecDBDeleted</strong></p></td>
<td><p>0 x 40000</p></td>
<td><p>Gibt an, dass der Datensatz bereits aus der Datenquelle gelöscht wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecDeleted</strong></p></td>
<td><p>0 x 4</p></td>
<td><p>Gibt an, dass der Datensatz gelöscht wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecIntegrityViolation</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da der Benutzer Integritätseinschränkungen verletzte.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecInvalid</strong></p></td>
<td><p>0 x 10</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da seine Textmarke ungültig ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMaxChangesExceeded</strong></p></td>
<td><p>0 x 2000</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da es zu viele ausstehende Änderungen gab.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecModified</strong></p></td>
<td><p>0x2</p></td>
<td><p>Gibt an, dass der Datensatz geändert wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMultipleChanges</strong></p></td>
<td><p>0 x 40</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da sich dies auf mehrere Datensätze ausgewirkt hätte.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecNew</strong></p></td>
<td><p>0x1</p></td>
<td><p>Gibt an, dass der Datensatz neu ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecObjectOpen</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Gibt an, dass der Datensatz aufgrund eines Konflikts mit einem geöffneten Speicherobjekt nicht gespeichert wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecOK</strong></p></td>
<td><p>0</p></td>
<td><p>Gibt an, dass der Datensatz erfolgreich aktualisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecOutOfMemory</strong></p></td>
<td><p>0 x 8000</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da der Computer keinen Arbeitsspeicher mehr zur Verfügung hat.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecPendingChanges</strong></p></td>
<td><p>0 x 80</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da er sich auf eine ausstehende Einfügung bezieht.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecPermissionDenied</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da der Benutzer über unzureichende Berechtigungen verfügt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecSchemaViolation</strong></p></td>
<td><p>0 x 20000</p></td>
<td><p>Gibt an, dass der Datensatz nicht gespeichert wurde, da er gegen die Struktur der zugrunde liegenden Datenbank verstößt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecUnmodified</strong></p></td>
<td><p>0 x 8</p></td>
<td><p>Gibt an, dass der Datensatz nicht geändert wurde.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

AdoEnums.RecordStatus.

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CANCELED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.CANTRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CONCURRENCYVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.DBDELETED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.DELETED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.INTEGRITYVIOLATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.INVALID</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.MODIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.NEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.OK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OUTOFMEMORY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.PENDINGCHANGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.PERMISSIONDENIED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.SCHEMAVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.UNMODIFIED</p></td>
</tr>
</tbody>
</table>

