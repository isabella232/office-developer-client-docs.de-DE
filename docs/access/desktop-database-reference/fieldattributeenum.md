---
title: FieldAttributeEnum (Access Desktop Database Reference)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292601"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**Gilt für**: Access 2013, Office 2013

Gibt mindestens ein Attribut eines [Field](field-object-ado.md)-Objekts an.

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
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Gibt an, dass der Anbieter Feldwerte zwischenspeichert und dass nachfolgende Lesevorgänge aus dem Cache durchgeführt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>Gibt an, dass das Feld Daten fester Länge enthält.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Gibt an, dass das Feld einen Kapitelwert enthält, der ein bestimmtes untergeordnetes Recordset angibt, das sich auf dieses übergeordnete Feld bezieht. Kapitelfelder werden normalerweise zur Datenstrukturierung oder für Filter verwendet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Gibt an, dass das Feld angibt, dass die Ressource, die vom Datensatz dargestellt wird, eine Auflistung anderer Ressourcen ist, wie z. B. ein Ordner, statt eine einfache Ressource, wie z. B. eine Textdatei.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Gibt an, dass das Feld den Standarddatenstrom für die Ressource enthält, die vom Datensatz dargestellt wird. Der Standarddatenstrom kann beispielsweise der HTML-Inhalt eines Stammordners auf einer Website sein, der automatisch bei Angabe der Stamm-URL bereitgestellt wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>Gibt an, dass das Feld Nullwerte annimmt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Gibt an, dass das Feld die URL enthält, die die Ressource aus dem Datenspeicher bezeichnet, der vom Datensatz dargestellt wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldLong</strong></p></td>
<td><p>0x80</p></td>
<td><p>Gibt an, dass es sich bei dem Feld um ein langes binäres Feld handelt. Gibt außerdem an, dass Sie die Methoden <a href="appendchunk-method-ado.md">AppendChunk</a> und <a href="getchunk-method-ado.md">GetChunk</a> verwenden können.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0x40</p></td>
<td><p>Gibt an, dass Sie Nullwerte aus dem Feld lesen können.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>Gibt an, dass das Feld verzögert ist – das heißt, die Feldwerte werden von der Datenquelle nicht mit dem gesamten Datensatz abgerufen, sondern nur, wenn Sie ausdrücklich darauf zugreifen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Gibt an, dass das Feld einen numerischen Wert aus einer Spalte darstellt, die negative Skalierungswerte unterstützt. Der Maßstab wird durch die <a href="numericscale-property-ado.md">NumericScale</a>-Eigenschaft angegeben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0x100</p></td>
<td><p>Gibt an, dass das Feld einen permanenten Zeilenbezeichner enthält, in den nicht geschrieben werden kann und der keinen Zweck hat, außer die Zeile zu identifizieren (wie Datensatznummer, eindeutiger Bezeichner usw.).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0x200</p></td>
<td><p>Gibt an, dass das Feld einen Zeit- und Datumstempel zum Verfolgen von Aktualisierungen enthält.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0x8</p></td>
<td><p>Gibt an, dass der Anbieter nicht ermitteln kann, ob Sie in das Feld schreiben können.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>-1<br />
0xFFFFFFFF</p></td>
<td><p>Gibt an, dass der Anbieter die Feldattribute nicht angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>Gibt an, dass Sie in das Feld schreiben können.</p></td>
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
<td><p>AdoEnums. Fieldattribute. CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. FIXED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. isNULLable</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. LONG</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. MAYBENULL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. MAYDEFER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. NEGATIVESCALE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. ROWID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. ROWVERSION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. UNKNOWNUPDATABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. unSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. AKTUALISIERBAR</p></td>
</tr>
</tbody>
</table>

