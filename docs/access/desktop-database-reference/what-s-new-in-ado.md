---
title: Neuerungen in ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 042ede650e6658ef346177491f95e976839c96e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568320"
---
# <a name="whats-new-in-ado"></a>Neuigkeiten in ADO

**Gilt für**: Access 2013, Office 2013 
 
Die folgenden neuen Features und die folgende erweiterte Dokumentation sind in der Version ADO 2.5 enthalten. In dieser Liste werden ADO, ADO MD und ADOX behandelt.

## <a name="new-features"></a>Neue Features

- **[Datensätze und Datenströme](chapter-10-records-and-streams.md)**

  In dieser Version von ADO wird das [Record-Objekt](record-object-ado.md) eingeführt, das Elemente wie Verzeichnisse und Dateien in einem Dateisystem sowie Ordner und Nachrichten in einem E-Mail-System darstellen und verwalten kann. Durch ein **Record**-Objekt kann auch eine Zeile in einem [Recordset](recordset-object-ado.md)-Objekt dargestellt werden, obwohl die Objekte **Record** und **Recordset** über unterschiedliche Methoden und Eigenschaften verfügen.

  Das neue [Stream](stream-object-ado.md)-Objekt ermöglicht das Lesen, Schreiben und Verwalten des binären Byte- oder Textdatenstroms, aus dem ein Datei- oder Nachrichtendatenstrom besteht.

- **[URL-Verwendung](absolute-and-relative-urls.md)**

  In dieser Version wird außerdem die Verwendung von URLs (Uniform Resource Locators) als Alternative zu Verbindungszeichenfolgen und Befehlstext zum Benennen von Datenspeicherobjekten eingeführt. URLs können mit den vorhandenen Objekten [Connection](connection-object-ado.md) und **Recordset** sowie mit den neuen Objekten **Record** und **Stream** verwendet werden.

  In dieser Version von ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* durch den auf das Windows 2000-Dateisystem zugegriffen wird, das vorhandene HTTP-Schema erkannt.

- **[Spezielle Felder für Dokumentquellenanbieter](records-and-provider-supplied-fields.md)**

  Mit einer speziellen Anbieterklasse, den *Dokumentquellenanbietern*, werden Ordner und Dokumente verwaltet. Wenn durch ein **Record**-Objekt ein Dokument dargestellt oder durch ein **Recordset**-Objekt ein Dokumentordner dargestellt wird, werden diese Objekte vom Dokumentquellenanbieter mit einem eindeutigen Satz Felder aufgefüllt, in dem die Merkmale des Dokuments beschrieben sind. Diese Felder bilden eine *Ressource* **Datensatz** oder **Recordset**.

## <a name="new-reference-topics"></a>Neue Referenzthemen

### <a name="properties"></a>Eigenschaften

Die folgenden neuen Eigenschaften sind in dieser Version enthalten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaft</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="charset-property-ado.md">Charset</a></p></td>
<td><p>Der Zeichensatz wird angegeben, in den der Inhalt eines <strong>Stream</strong>-Textobjekts übersetzt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Es wird angegeben, ob sich die aktuelle Position am Ende des Datenstroms befindet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Das als Linientrennzeichen in <strong>Stream</strong>-Textobjekten zu verwendende binäre Zeichen wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Es werden die verfügbaren Berechtigungen zum Ändern von Daten in einem <strong>Connection</strong>-, <strong>Record</strong>- oder <strong>Stream</strong>-Objekt angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Eine absolute URL-Zeichenfolge wird angegeben, die auf das übergeordnete <strong>Record</strong>-Objekt des aktuellen <strong>Record</strong>-Objekts zeigt.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Die aktuelle Position in einem <strong>Stream</strong>-Objekt wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Der Typ eines <strong>Record</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Größe</a></p></td>
<td><p>Die Größe des Datenstroms wird als Byteanzahl angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Die Entität wird angegeben, die durch das <strong>Record</strong>-Objekt dargestellt wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Für alle entsprechenden Objekte wird angegeben, ob der Status des Objekts open oder closed entspricht. Für alle entsprechenden Objekte, durch die eine asynchrone Methode ausgeführt wird, wird angegeben, ob der aktuelle Status des Objekts connecting, executing oder retrieving entspricht.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Typ</a></p></td>
<td><p>Der Typ der im <strong>Stream</strong>-Objekt enthaltenen Daten (Binärdaten oder Textdaten) wird angegeben.</p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a>Methoden

Die folgenden neuen Methoden sind in dieser Version enthalten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Methode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Kopiert die angegebene Anzahl von Zeichen oder Bytes (je nach <strong>Typ)</strong>im <strong>Stream-Objekt</strong> <strong></strong> in ein anderes <strong>Stream-Objekt.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Flush</a></p></td>
<td><p>Es wird erzwungen, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts in das zugrunde liegende Objekt übernommen wird, das dem <strong>Stream</strong>-Objekt zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Ein <strong>Recordset</strong>-Objekt wird zurückgegeben, dessen Zeilen die Daten und Unterverzeichnisse in dem durch dieses <strong>Record</strong>-Objekt dargestellten Verzeichnis darstellen.</p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Der Inhalt einer vorhandenen Datei wird in ein <strong>Stream</strong>-Objekt geladen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">Öffnen</a></p></td>
<td><p>Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Öffnen</a></p></td>
<td><p>Ein <strong>Stream</strong>-Objekt zum Ändern von Datenströmen von Binär- oder Textdaten wird geöffnet.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Lesen</a></p></td>
<td><p>Eine angegebene Anzahl von Bytes aus einem binären <strong>Stream</strong>-Objekt wird abgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">Readtext</a></p></td>
<td><p>Eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt wird abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Der Binärinhalt eines <strong>Stream</strong>-Objekts wird in einer Datei gespeichert.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Die Position, die das Ende des Datenstroms darstellt, wird festgelegt.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Beim Lesen eines <strong>Stream</strong>-Textobjekts wird eine gesamte Zeile übersprungen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Binärdaten werden in ein <strong>Stream</strong>-Objekt geschrieben.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">Writetext</a></p></td>
<td><p>Eine angegebene Textzeichenfolge wird in ein <strong>Stream</strong>-Objekt geschrieben.</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Neue und erweiterte Dokumentation

- **[Codebeispielthemen](ado-code-examples.md)**

  Die Beispiele wurden um Codebeispiele erweitert, die in Microsoft Visual C++ und Microsoft Visual J++ geschrieben wurden. Sie können diese Codebeispiele kopieren und in den Editor einfügen.

- **[Anbieterthemen](appendix-a-providers.md)**

  Es ist ein neues Thema enthalten, in dem die Verwendung von ADO mit dem [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) erläutert wird.

- **[Programmieren mit ADO](appendix-c-programming-with-ado.md)**

  Dieser neue Abschnitt enthält Tipps und Tricks für das Verwenden von ADO mit verschiedenen Programmiersprachen. Sie enthält die vorhandenen Syntaxindizes für die Visual C++-Erweiterungen für ADO und ADO/WFC sowie neue Informationen speziell für Entwickler, die Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ oder Microsoft Visual J++ verwenden.

