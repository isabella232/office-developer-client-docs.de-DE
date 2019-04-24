---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295485"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Gilt für**: Access 2013, Office 2013

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


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

