---
title: EventStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49f584603c25997e1b01b94f23aaf9f5429a9e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472629"
---
# <a name="eventstatusenum"></a>EventStatusEnum


**Betrifft**: Access 2013 | Office 2013

Gibt den aktuellen Status der Ausführung eines Ereignisses an.

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
<td><p><strong>adStatusCancel fest</strong></p></td>
<td><p>4</p></td>
<td><p>Fordert den Abbruch des Vorgangs an, der zum Ereignis führte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt an, dass der Vorgang keinen Abbruch der ausstehenden Operation anfordern kann.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt an, dass der Vorgang, der das Ereignis verursachte, aufgrund eines Fehlers oder mehrerer Fehler fehlschlug.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>1</p></td>
<td><p>Gibt an, dass der Vorgang, der das Ereignis verursachte, erfolgreich war.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>5</p></td>
<td><p>Verhindert nachfolgende Benachrichtigungen, bevor die Ereignismethode die Ausführung beendet hat.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

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
<td><p>AdoEnums.EventStatus.CANCEL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventStatus.CANTDENY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventStatus.ERRORSOCCURRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventStatus.OK</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventStatus.UNWANTEDEVENT</p></td>
</tr>
</tbody>
</table>

