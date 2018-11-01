---
title: Relation Members (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d6aceacf462898628b0aee9e406860def9474c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889917"
---
# <a name="relation-members-dao"></a>Relation Members (DAO)


**Betrifft**: Access 2013, Office 2013

Ein Relation-Objekt stellt eine Beziehung zwischen Feldern in Tabellen oder Abfragen dar (gilt nur für Microsoft Access-Datenbanken).

## <a name="methods"></a>Methoden

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="field-object-dao.md">Field</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="relation-attributes-property-dao.md">Attribute</a></strong></p></td>
<td><p>Legt einen Wert fest, der mindestens ein Merkmal eines <strong>Relation</strong>-Objekts angibt, oder gibt den betreffenden Wert zurück. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-fields-property-dao.md">Felder</a></strong></p></td>
<td><p>Gibt eine <strong>Fields</strong>-Auflistung zurück, die alle gespeicherten <strong>Field</strong>-Objekte für das angegebene Objekt enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></p></td>
<td><p>Legt den Namen der Fremdtabelle in einer Beziehung fest oder gibt den Namen zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></p></td>
<td><p>Legt einen Wert für ein <strong>Relation</strong>-Objekt fest, der angibt, ob die Beziehung berücksichtigt werden soll, wenn ein Teilreplikat von einem vollständigen Replikat aufgefüllt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Datenbanken). <strong>Boolean</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-table-property-dao.md">Tabelle</a></strong></p></td>
<td><p>Gibt den Namen der Primärtabelle eines <strong><a href="relation-object-dao.md">Relation</a></strong> -Objekts an. Dieser Name sollte mit dem Wert der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft eines <strong><a href="tabledef-object-dao.md">TableDef</a></strong> - oder <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekts übereinstimmen (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

