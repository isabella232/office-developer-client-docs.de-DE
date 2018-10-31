---
title: ConnectPromptEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f10fd9fada954bb5e3a356961636b2022c73bae3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862170"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum

**Betrifft**: Access 2013 | Office 2013

Gibt an, ob ein Dialogfeld angezeigt werden soll, um beim Öffnen einer Verbindung mit einer Datenquelle fehlende Parameter anzufordern.

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
<td><p><strong>adPromptAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Fordert immer auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>2</p></td>
<td><p>Fordert auf, wenn weitere Informationen erforderlich sind.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3</p></td>
<td><p>Fordert auf, wenn weitere Informationen erforderlich sind, optionale Parameter jedoch nicht zulässig sind.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4</p></td>
<td><p>Fordert nie auf.</p></td>
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
<td><p>AdoEnums.ConnectPrompt.ALWAYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.COMPLETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectPrompt.COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.NEVER</p></td>
</tr>
</tbody>
</table>

