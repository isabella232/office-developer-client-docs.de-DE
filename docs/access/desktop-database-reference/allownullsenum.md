---
title: AllowNullsEnum (Access PC-Datenbank-Referenz)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04e67584e0f0c2eeb5a12e34fdf98a84cc1da852
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474323"
---
# <a name="allownullsenum"></a>AllowNullsEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob Datensätze mit Nullwerten indiziert werden.

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
<td><p><strong>adIndexNullsAllow</strong></p></td>
<td><p>0</p></td>
<td><p>Der Index lässt Einträge mit nullwertigen Schlüsselspalten zu. Wenn ein Nullwert in eine Schlüsselspalte eingegeben wird, wird der Eintrag in den Index eingefügt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1</p></td>
<td><p>Standardeinstellung. Der Index lässt keine Einträge mit nullwertigen Schlüsselspalten zu. Wenn ein Nullwert in eine Schlüsselspalte eingegeben wird, tritt ein Fehler auf.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>2</p></td>
<td><p>Der Index fügt keine Einträge mit nullwertigen Schlüsselspalten ein. Wenn ein Nullwert in eine Schlüsselspalte eingegeben wird, wird der Eintrag ignoriert, und es tritt kein Fehler auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>4</p></td>
<td><p>Der Index fügt keine Einträge mit einer nullwertigen Schlüsselspalte ein. Bei einem Index mit einem mehrspaltigen Schlüssel wird der Eintrag ignoriert und kein Fehler ausgelöst, wenn ein Nullwert in eine Spalte eingegeben wird.</p></td>
</tr>
</tbody>
</table>

