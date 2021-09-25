---
title: EventStatusEnum (Access-Desktopdatenbankreferenz)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a703dcafc981bd5663d01329330dd3cd2b0e23b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602682"
---
# <a name="eventstatusenum"></a>EventStatusEnum

**Gilt für**: Access 2013, Office 2013

Gibt den aktuellen Status der Ausführung eines Ereignisses an.

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
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>4 </p></td>
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


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

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

