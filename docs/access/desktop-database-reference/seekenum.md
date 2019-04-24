---
title: SeekEnum (Access Desktop Database Reference)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314658"
---
# <a name="seekenum"></a>SeekEnum

**Gilt für**: Access 2013, Office 2013

Gibt die Art der auszuführenden [Suche](seek-method-ado.md) an.

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
<td><p>adSeekFirstEQ</p></td>
<td><p>1</p></td>
<td><p>Sucht den ersten Schlüssel, der <em>KeyValues</em> entspricht.</p></td>
</tr>
<tr class="even">
<td><p>adSeekLastEQ</p></td>
<td><p>2</p></td>
<td><p>Sucht den letzten Schlüssel, der <em>KeyValues</em> entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>adSeekAfterEQ</p></td>
<td><p>4</p></td>
<td><p>Sucht entweder einen Schlüssel, der <em>KeyValues</em> entspricht, oder direkt nach der Stelle, an der diese Übereinstimmung aufgetreten wäre.</p></td>
</tr>
<tr class="even">
<td><p>adSeekAfter</p></td>
<td><p>8</p></td>
<td><p>Sucht einen Schlüssel direkt nach der Stelle, an der eine Übereinstimmung mit <em>KeyValues</em> aufgetreten wäre.</p></td>
</tr>
<tr class="odd">
<td><p>adSeekBeforeEQ</p></td>
<td><p>16</p></td>
<td><p>Sucht einen Schlüssel, der entweder <em>KeyValues</em> entspricht, oder direkt vor der Stelle, an der diese Übereinstimmung aufgetreten wäre.</p></td>
</tr>
<tr class="even">
<td><p>adSeekBefore</p></td>
<td><p>32</p></td>
<td><p>Sucht einen Schlüssel direkt vor der Stelle, an der eine Übereinstimmung mit <em>KeyValues</em> aufgetreten wäre.</p></td>
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
<td><p>AdoEnums. Seek. FIRSTEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. LASTEQ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Seek. AFTEREQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. AFTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Seek. BEFOREEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. BEFORE</p></td>
</tr>
</tbody>
</table>

