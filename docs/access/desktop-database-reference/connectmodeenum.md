---
title: ConnectModeEnum (Access Desktop Database Reference)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295695"
---
# <a name="connectmodeenum"></a>ConnectModeEnum

**Gilt für**: Access 2013, Office 2013

Gibt die verfügbaren Berechtigungen zum Ändern von Daten in einer [Verbindung](connection-object-ado.md) an, wobei ein [Datensatz](record-object-ado.md) geöffnet wird oder Werte für die [Mode](mode-property-ado.md)-Eigenschaft der **Record**- und [Stream](stream-object-ado.md)-Objekte angegeben werden.

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
<td><p><strong>adModeRead</strong></p></td>
<td><p>1</p></td>
<td><p>Gibt nur schreibgeschützte Berechtigungen an.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt Lese-/Schreibberechtigungen an.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0x400000</p></td>
<td><p>Wird zusammen mit den anderen <em>*ShareDeny*</em> -Werten (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>oder <strong>adModeShareDenyRead</strong>) verwendet, um Freigabeeinschränkungen an alle Unterdatensätze des aktuellen <strong>Datensatzes</strong>zu verteilen. Sie hat keine Auswirkungen, wenn der <strong>Datensatz</strong> keine untergeordneten Elemente aufweist.</p><p>Wenn es nur mit <strong>adModeShareDenyNone</strong> verwendet wird, wird ein Laufzeitfehler generiert. Sie kann jedoch mit <strong>adModeShareDenyNone</strong> verwendet werden, wenn Sie mit anderen Werten kombiniert wird. Sie können beispielsweise &quot; <strong>adModeRead</strong> oder <strong>adModeShareDenyNone</strong> oder <strong>adModeRecursive</strong>&quot;verwenden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>16</p></td>
<td><p>Ermöglicht anderen Personen, eine Verbindung mit allen Berechtigungen zu öffnen. Weder der Lese- noch der Schreibzugriff kann anderen Personen verweigert werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>4</p></td>
<td><p>Verhindert, dass andere Personen eine Verbindung mit Leseberechtigungen öffnen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>8</p></td>
<td><p>Verhindert, dass andere Personen eine Verbindung mit Schreibberechtigungen öffnen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>12</p></td>
<td><p>Verhindert, dass andere Personen eine Verbindung öffnen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Standardwert. Gibt an, dass die Berechtigungen noch nicht festgelegt wurden oder nicht ermittelt werden können.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt lesegeschützte Berechtigungen an.</p></td>
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
<td><p>AdoEnums. ConnectMode. READ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. READWRITE</p></td>
</tr>
<tr class="odd">
<td><p>(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. SHAREDENYNONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. SHAREDENYREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. SHAREDENYWRITE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. SHAREEXCLUSIVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. UNKNOWN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. WRITE</p></td>
</tr>
</tbody>
</table>

