---
title: Datensätze und vom Anbieter bereitgestellte Felder
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ebbfeb303bb575928f09858db5d3a34cf2171ce0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300756"
---
# <a name="records-and-provider-supplied-fields"></a>Datensätze und vom Anbieter bereitgestellte Felder

**Gilt für**: Access 2013, Office 2013

Wenn ein [Record](record-object-ado.md)-Objekt geöffnet wird, kann die Quelle die aktuelle Zeile eines geöffneten [Recordsets](recordset-object-ado.md), eine absolute URL oder eine relative URL in Verbindung mit einem geöffneten [Connection](connection-object-ado.md)-Objekt sein.

Wenn das **Record** -Objekt aus einem **Recordset** -Objekt geöffnet wird, enthält die **Fields**-Auflistung des [Record](fields-collection-ado.md) -Objekts alle Felder aus dem **Recordset** sowie alle durch den zugrunde liegenden Anbieter hinzugefügten Felder.

Durch den Anbieter können zusätzliche Felder eingefügt werden, die als ergänzende Merkmale des **Record** -Objekts dienen. Daher verfügt ein **Record** -Objekt möglicherweise über eindeutige Felder, die im gesamten **Recordset** -Objekt oder in einem aus einer anderen Zeile des **Recordset** -Objekts abgeleiteten **Record** -Objekt nicht enthalten sind.

Beispielsweise können alle Zeilen eines **Recordset-Objekts** , das von einer e-Mail-Datenquelle abgeleitet wurde, Spalten wie from, to und Subject aufweisen. A **Record** derived from that **Recordset** will have the same fields. However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).

Obwohl das **Record** -Objekt und die aktuelle Zeile des **Recordset** -Objekts die gleichen Felder enthalten, unterscheiden sie sich, da die Objekte **Record** und **Recordset** über verschiedene Methoden und Eigenschaften verfügen.

Ein sowohl in **Record** als auch in **Recordset** enthaltenes Feld kann für jedes der Objekte geändert werden. Das Feld kann jedoch nicht für das **Record** -Objekt gelöscht werden, da vom zugrunde liegenden Anbieter möglicherweise das Festlegen des Felds auf Null unterstützt wird.

Nach dem Öffnen des **Record** -Objekts können Sie programmatisch Felder hinzufügen. Sie können auch hinzugefügte Felder löschen, Sie können jedoch keine Felder aus dem ursprünglichen **Recordset** -Objekt löschen.

Sie können das **Record** -Objekt auch direkt über eine URL öffnen. In diesem Fall hängen die dem **Record** -Objekt hinzugefügten Felder vom zugrunde liegenden Anbieter ab. Zurzeit wird durch die meisten Anbieter ein Satz Felder hinzugefügt, in denen die Entität beschrieben wird, die durch das **Record** -Objekt dargestellt wird. Wenn die Entität aus einem Bytedatenstrom besteht, z. B. aus einer einfachen Datei, kann ein [Stream](stream-object-ado.md)-Objekt normalerweise aus dem **Record** -Objekt geöffnet werden.

## <a name="special-fields-for-document-source-providers"></a>Spezielle Felder für Dokumentquellenanbieter

Mit einer speziellen Anbieterklasse, den *Dokumentquellenanbietern*, werden Ordner und Dokumente verwaltet. Wenn durch ein **Record**-Objekt ein Dokument dargestellt oder durch ein **Recordset**-Objekt ein Dokumentordner dargestellt wird, werden diese Objekte vom Dokumentquellenanbieter mit einem eindeutigen Satz Felder aufgefüllt, in dem die Merkmale des Dokuments anstelle des eigentlichen Dokuments selbst beschrieben sind. Normalerweise enthält ein Feld einen Verweis auf das **Stream**-Objekt, durch das das Dokument dargestellt wird.

Diese Felder stellen einen Ressourcen **datensatz** oder ein **Recordset** dar und werden in [Anhang A: Anbieter](appendix-a-providers.md) für die Anbieter aufgelistet, von denen sie unterstützt werden.

Die **Fields** -Auflistung des **Record** - oder **Recordset** -Objekts einer Ressource wird von zwei Konstanten indiziert, um ein Paar häufig verwendeter Felder abzurufen. Durch die **Value**-Eigenschaft des [Field](value-property-ado.md) -Objekts wird der gewünschte Inhalt zurückgegeben.

  - Das Feld, auf das mit der **adDefaultStream** -Konstante zugegriffen wird, enthält einen dem **Record** - oder **Recordset** -Objekt zugeordneten Standarddatenstrom. Dem Objekt wird vom Anbieter ein Standarddatenstrom zugewiesen.

  - Das Feld, auf das mit der **adRecordURL** -Konstante zugegriffen wird, enthält die absolute URL, durch die das Dokument identifiziert wird.

Die [Properties](properties-collection-ado.md)-Auflistung der Objekte **Record** und **Field** wird von einem Dokumentquellenanbieter nicht unterstützt. Der Inhalt der **Properties** -Auflistung entspricht für solche Objekte Null.

Von einem Dokumentquellenanbieter kann eine anbieterspezifische Eigenschaft wie z. B **Datasource Type** hinzugefügt werden, um zu identifizieren, ob es sich um einen Dokumentquellenanbieter handelt. Weitere Informationen zum Ermitteln des Anbietertyps finden Sie in der Anbieterdokumentation.

## <a name="resource-recordset-columns"></a>Spalten von Ressourcenrecordsets

Ein *Ressourcenrecordset* besteht aus den folgenden Spalten.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Spaltenname</p></th>
<th><p>Typ</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RESOURCE_PARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Schreibgeschützt. Die URL der Ressource wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_PARENTNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Schreibgeschützt. Die absolute URL des übergeordneten Datensatzes wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ABSOLUTEPARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Schreibgeschützt. Die absolute URL der Ressource, die der Verkettung von PARENTNAME und PARSENAME entspricht, wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISHIDDEN</p></td>
<td><p>Boolean</p></td>
<td><p>True, wenn die Ressource ausgeblendet ist. Es werden nur Zeilen zurückgegeben, wenn durch den Befehl, durch den das Rowset erstellt wird, explizit Zeilen ausgewählt werden, bei denen RESOURCE_ISHIDDEN True entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISREADONLY</p></td>
<td><p>Boolean</p></td>
<td><p>True, wenn die Ressource schreibgeschützt ist. Es wird versucht, diese Ressource mit DBBINDFLAG_WRITE zu öffnen, bei DB_E_READONLY schlägt der Vorgang fehl. Diese Eigenschaft kann auch dann bearbeitet werden, wenn die Ressource nur zum Lesen geöffnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTTYPE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Die wahrscheinliche Verwendung des Dokuments wird angegeben - z. B. ein juristischer Schriftsatz. Dies entspricht möglicherweise der Office-Vorlage, die zum Erstellen des Dokuments verwendet wird.&quot;&quot;</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CONTENTCLASS</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Gibt den MIME-Typ des Dokuments an, der das Format wie " &quot;Text/HTML&quot;" angibt.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTLANGUAGE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Die Sprache, in der der Inhalt gespeichert wird, wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CREATIONTIME</p></td>
<td><p>Dateien</p></td>
<td><p>Schreibgeschützt. Es wird eine FILETIME-Struktur angegeben, die die Uhrzeit der Erstellung der Ressource enthält. Die Uhrzeit wird im UTC-Format (Coordinated Universal Time, koordinierte Weltzeit) angegeben.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_LASTACCESSTIME</p></td>
<td><p>Dateien</p></td>
<td><p>Schreibgeschützt. Es wird eine FILETIME-Struktur angegeben, die die Uhrzeit des letzten Zugriffs auf die Ressource enthält. Die Uhrzeit wird im UTC-Format angegeben. Die FILETIME-Elemente sind Null, wenn dieses Zeitelement vom Anbieter nicht unterstützt wird.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_LASTWRITETIME</p></td>
<td><p>Dateien</p></td>
<td><p>Schreibgeschützt. Es wird eine FILETIME-Struktur angegeben, die die Uhrzeit des letzten Schreibvorgangs für die Ressource enthält. Die Uhrzeit wird im UTC-Format angegeben. Die FILETIME-Elemente sind Null, wenn dieses Zeitelement vom Anbieter nicht unterstützt wird.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_STREAMSIZE</p></td>
<td><p>asUnsignedBigInt</p></td>
<td><p>Schreibgeschützt. Die Größe des Standarddatenstroms der Ressource wird in Byte angegeben.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISCOLLECTION</p></td>
<td><p>Boolean</p></td>
<td><p>Schreibgeschützt. True, wenn die Ressource eine Auflistung, z. B. ein Verzeichnis, ist. False, wenn die Ressource eine einfache Datei ist.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISSTRUCTUREDDOCUMENT</p></td>
<td><p>Boolean</p></td>
<td><p>True, wenn die Ressource ein strukturiertes Dokument ist. False, wenn die Ressource kein strukturiertes Dokument ist. Sie kann eine Auflistung oder eine einfache Datei sein.</p></td>
</tr>
<tr class="odd">
<td><p>DEFAULT_DOCUMENT</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Schreibgeschützt. Es wird angegeben, dass diese Ressource eine URL zum einfachen Standarddokument eines Ordners oder eines strukturierten Dokuments enthält. Wird verwendet, wenn der Standarddatenstrom von einer Ressource angefordert wird. Diese Eigenschaft ist für eine einfache Datei leer.</p></td>
</tr>
<tr class="even">
<td><p>CHAPTERED_CHILDREN</p></td>
<td><p>AdChapter</p></td>
<td><p>Schreibgeschützt. Optional. Das Kapitel des Rowsets, das die untergeordneten Elemente der Ressource enthält, wird angegeben. (Vom <em>OLE DB-Anbieter für Internet Publishing</em> wird diese Spalte nicht verwendet.)</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_DISPLAYNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Schreibgeschützt. Der Anzeigename der Ressource wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISROOT</p></td>
<td><p>Boolean</p></td>
<td><p>Schreibgeschützt. True, wenn die Ressource der Stamm einer Auflistung oder eines strukturierten Dokuments ist.</p></td>
</tr>
</tbody>
</table>

