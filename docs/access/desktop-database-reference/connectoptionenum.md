---
title: ConnectOptionEnum (Access Desktop Database Reference)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295681"
---
# <a name="connectoptionenum"></a>ConnectOptionEnum

**Gilt für**: Access 2013, Office 2013

Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.

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
<td><p>AdoEnums. ConnectOption. ASYNCCONNECT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectOption. CONNECTUNSPECIFIED</p></td>
</tr>
</tbody>
</table>

