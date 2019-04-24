---
title: EventStatusEnum (Access Desktop Database Reference)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293273"
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
<td><p><strong>adStatusCancel fest</strong></p></td>
<td><p>4</p></td>
<td><p>Fordert den Abbruch des Vorgangs an, der zum Ereignis führte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCantDeny festgelegt</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt an, dass der Vorgang keinen Abbruch der ausstehenden Operation anfordern kann.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusErrorsOccurred festgelegt</strong></p></td>
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


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

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
<td><p>AdoEnums. EventStatus. CANCEL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventStatus. CANTDENY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventStatus. ERRORSOCCURRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventStatus. OK</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventStatus. UNWANTEDEVENT</p></td>
</tr>
</tbody>
</table>

