---
title: ResyncEnum (Access PC-Datenbank-Referenz)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3607c0796edb58a6d4227fee09a658220deabfe7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475889"
---
# <a name="resyncenum"></a>ResyncEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob die zugrunde liegenden Werte durch einen Aufruf von [Resync](resync-method-ado.md) überschrieben werden.

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
<td><p><strong>adResyncAllValues</strong></p></td>
<td><p>2</p></td>
<td><p>Standardwert. Überschreibt Daten, und die ausstehenden Aktualisierungen werden abgebrochen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUnderlyingValues</strong></p></td>
<td><p>1</p></td>
<td><p>Überschreibt keine Daten, und die ausstehenden Aktualisierungen werden nicht abgebrochen.</p></td>
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
<td><p>AdoEnums.Resync.ALLVALUES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Resync.UNDERLYINGVALUES</p></td>
</tr>
</tbody>
</table>

