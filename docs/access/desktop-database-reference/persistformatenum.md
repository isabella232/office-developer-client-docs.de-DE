---
title: PersistFormatEnum (Access PC-Datenbank-Referenz)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3254d60c6daa032857227b1f16f9a9c085164dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473868"
---
# <a name="persistformatenum"></a>PersistFormatEnum


**Betrifft**: Access 2013 | Office 2013

Gibt das Format an, in dem ein [Recordset](recordset-object-ado.md) gespeichert werden soll.

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
<td><p><strong>adPersistADTG</strong></p></td>
<td><p>0</p></td>
<td><p>Gibt das Microsoft Advanced Data TableGram-Format (ADTG) an.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistADO</strong></p></td>
<td><p>1</p></td>
<td><p>Gibt an, dass das XML-Format von ADO verwendet wird. Dieser Wert entspricht AdPersistXML und ist zum Zwecke der Abwärtskompatibilität eingeschlossen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPersistXML</strong></p></td>
<td><p>1</p></td>
<td><p>Gibt das XML-Format an.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistProviderSpecific</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt an, dass der Anbieter das <strong>Recordset</strong> mit seinem eigenen Format beibehält.</p></td>
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
<td><p>AdoEnums.PersistFormat.ADTG</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PersistFormat.XML</p></td>
</tr>
</tbody>
</table>

