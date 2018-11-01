---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3c3ddd8174a646bccd37cec758e85e17f4cdaec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882777"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Betrifft**: Access 2013, Office 2013

Gibt das Verhalten der [CopyRecord](copyrecord-method-ado.md)-Methode an.

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
<td><p><strong>adCopyAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Gibt an, dass der Anbieter <em>Quelle</em> versucht, die Kopie mithilfe von Download- und Uploadvorgängen zu simulieren, wenn diese Methode aufgrund des <em>Ziels</em> fehlschlägt, das sich auf einem anderen Server befindet, oder wenn sie von einem anderen Anbieter als <em>Quelle</em> bedient wird. Beachten Sie, dass abweichende Anbieterfunktionen die Leistung einschränken oder zu Datenverlusten führen können.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>Kopiert das aktuelle Verzeichnis, aber keines seiner Unterverzeichnisse an das Ziel. Der Kopiervorgang ist nicht rekursiv.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Überschreibt die Datei oder das Verzeichnis, wenn das <em>Ziel</em> auf eine bereits vorhandene Datei oder ein bereits vorhandenes Verzeichnis verweist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Führt den Standardkopiervorgang aus: Der Vorgang schlägt fehl, wenn die Zieldatei oder das Zielverzeichnis bereits vorhanden ist, und der Vorgang rekursiv kopiert.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

