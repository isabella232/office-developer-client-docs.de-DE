---
title: ConnectOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2e8439099732cd3e1e9aa7531f5ae3be25d7ebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472987"
---
# <a name="connectoptionenum"></a>ConnectOptionEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.

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
<td><p><strong>adAsyncConnect</strong></p></td>
<td><p>16</p></td>
<td><p>Öffnet die Verbindung asynchron. Das <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a>-Ereignis kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adConnectUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Öffnet die Verbindung synchron.</p></td>
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
<td><p>AdoEnums.ConnectOption.ASYNCCONNECT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectOption.CONNECTUNSPECIFIED</p></td>
</tr>
</tbody>
</table>

