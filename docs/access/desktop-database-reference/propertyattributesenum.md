---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302877"
---
# <a name="propertyattributesenum"></a>PropertyAttributesEnum


**Gilt für**: Access 2013, Office 2013

Gibt die Attribute eines [Property](property-object-ado.md)-Objekts an.

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
<td><p><strong>adPropNotSupported</strong></p></td>
<td><p>0</p></td>
<td><p>Gibt an, dass die Eigenschaft vom Anbieter nicht unterstützt wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropRequired</strong></p></td>
<td><p>1</p></td>
<td><p>Gibt an, dass der Benutzer einen Wert für diese Eigenschaft angeben muss, bevor die Datenquelle initialisiert wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPropOptional</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt an, dass der Benutzer keinen Wert für diese Eigenschaft angeben muss, bevor die Datenquelle initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropRead</strong></p></td>
<td><p>512</p></td>
<td><p>Gibt an, dass der Benutzer die Eigenschaft lesen kann.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPropWrite</strong></p></td>
<td><p>1024</p></td>
<td><p>Gibt an, dass der Benutzer die Eigenschaft festlegen kann.</p></td>
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
<td><p>AdoEnums. PropertyAttributes. NOTSUPPORTED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. PropertyAttributes. REQUIRED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. PropertyAttributes. OPTIONAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. PropertyAttributes. READ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. PropertyAttributes. WRITE</p></td>
</tr>
</tbody>
</table>

