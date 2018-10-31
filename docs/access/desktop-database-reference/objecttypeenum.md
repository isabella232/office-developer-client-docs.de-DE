---
title: ObjectTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c5fb9dbf86823ab4d84327d97eceb037eb77dec0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863717"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**Betrifft**: Access 2013 | Office 2013

Gibt den Typ des Datenbankobjekts an, für das Berechtigungen oder Besitzrechte festgelegt werden sollen.

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
<td><p><strong>adPermObjColumn</strong></p></td>
<td><p>2</p></td>
<td><p>Bei dem Objekt handelt es sich um eine Spalte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjDatabase</strong></p></td>
<td><p>3</p></td>
<td><p>Bei dem Objekt handelt es sich um eine Datenbank.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjProcedure</strong></p></td>
<td><p>4</p></td>
<td><p>Bei dem Objekt handelt es sich um eine Prozedur.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>Bei dem Objekt handelt es sich um einen vom Anbieter definierten Typ. Es tritt ein Fehler auf, wenn der <em>ObjectType</em>-Parameter gleich <strong>adPermObjProviderSpecific</strong> ist und <em>ObjectTypeId</em> nicht angegeben ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjTable</strong></p></td>
<td><p>1</p></td>
<td><p>Bei dem Objekt handelt es sich um eine Tabelle.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjView</strong></p></td>
<td><p>5</p></td>
<td><p>Bei dem Objekt handelt es sich um eine Sicht.</p></td>
</tr>
</tbody>
</table>

