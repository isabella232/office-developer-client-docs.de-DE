---
title: Dynamische ADO-Eigenschaften
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab0d84931389aecb5bd495c884baa9163c52d4a6
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910922"
---
# <a name="ado-dynamic-properties"></a>Dynamische ADO-Eigenschaften

**Betrifft**: Access 2013, Office 2013

Dynamische Eigenschaften können den [Properties](properties-collection-ado.md)-Auflistungen der [Connection](connection-object-ado.md)-, [Command](command-object-ado.md)- oder [Recordset](recordset-object-ado.md)-Objekte hinzugefügt werden. Die Quelle für diese Eigenschaften ist ein Datenanbieter, wie z. B. der [OLE DB-Anbieter für SQL Server](microsoft-ole-db-provider-for-sql-server.md), oder ein Dienstanbieter, wie z. B. der [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Weitere Informationen zu einer bestimmten dynamischen Eigenschaft finden Sie in der Dokumentation des entsprechenden Datenanbieters oder Dienstanbieters.

Der [Dynamische ADO-Eigenschaftenindex](ado-dynamic-property-index.md) stellt einen Querverweis zwischen den ADO- und OLE DB-Namen der einzelnen dynamischen Standardeigenschaften des OLE DB-Anbieters bereit.

Die folgenden dynamischen Eigenschaften sind von besonderem Interesse und werden ebenfalls in den oben genannten Quellen dokumentiert. Die spezielle Funktionalität mit ADO ist in den unten aufgelisteten ADO-Hilfethemen dokumentiert.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Dynamische Eigenschaft</th>
<th>Beschreibung</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Optimieren der Leistung von</a></p></td>
<td><p>Es wird angegeben, ob für dieses Feld ein Index erstellt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>Gibt an, ob der OLE DB-Anbieter den Benutzer zur Eingabe von Initialisierungsinformationen auffordern soll.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Gibt einen Namen für das <strong>Recordset</strong>-Objekt an.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Gibt eine vom Benutzer bereitgestellte Befehlszeichenfolge an, die von der <strong>Resync</strong>-Methode ausgegeben wird, um die Daten in der Tabelle zu aktualisieren, die in der dynamischen <strong>Unique Table</strong>-Eigenschaft genannt ist.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></p></td>
<td><p><strong>Unique Table</strong> – gibt den Namen der Basistabelle, für das Aktualisierungen, einfügungen und Löschvorgänge zulässig sind.<br/><br/><strong>Unique Schema</strong> – gibt an, das Schema oder der Name des Besitzers der Tabelle.<br/><br/><strong>Unique Catalog</strong> – gibt den Katalog oder Name der Datenbank, die die Tabelle enthält.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a></p></td>
<td><p>Gibt an, ob auf die <strong>UpdateBatch</strong>-Methode ein impliziter Vorgang mit einer <strong>Resync</strong>-Methode folgt. Wenn dies der Fall ist, wird der Bereich des Vorgangs angegeben.</p></td>
</tr>
</tbody>
</table>

<br/>

