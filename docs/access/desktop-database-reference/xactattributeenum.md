---
title: XactAttributeEnum (Access Desktop Database Reference)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302569"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**Gilt für**: Access 2013, Office 2013

Gibt die Transaktionsattribute eines [Connection](connection-object-ado.md)-Objekts an.

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
<td><p><strong>adXactAbortRetaining</strong></p></td>
<td><p>262144</p></td>
<td><p>Führt Beibehaltungs Unterbrechungen aus; Das heißt, das Aufrufen von <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> startet automatisch eine neue Transaktion. Nicht alle Anbieter unterstützen dies.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>Führt Aufbewahrungspflichten aus; Das heißt, das Aufrufen von <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> startet automatisch eine neue Transaktion. Nicht alle Anbieter unterstützen dies.</p></td>
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
<td><p>AdoEnums. XactAttribute. ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. XactAttribute. COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

