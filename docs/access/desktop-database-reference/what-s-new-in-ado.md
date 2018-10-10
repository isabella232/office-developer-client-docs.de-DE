---
title: Was ist neu in ActiveX Data Objects (ADO)
TOCTitle: What's New in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86d3c151ac77ab4138afcd84ee2a14d94dd07aef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473620"
---
# <a name="whats-new-in-ado"></a>Neuigkeiten in ADO


**Betrifft**: Access 2013 | Office 2013 
 

Die folgenden neuen Features und die folgende erweiterte Dokumentation sind in der Version ADO 2.5 enthalten. In dieser Liste werden ADO, ADO MD und ADOX behandelt.

## <a name="new-features"></a>Neue Features

**[Datensätze und Datenströme](chapter-10-records-and-streams.md)**

In dieser Version von ADO wird das [Record](record-object-ado.md)-Objekt eingeführt, durch das z. B. Verzeichnisse und Dateien in einem Dateisystem oder Ordner und Nachrichten in einem E-Mail-System dargestellt und verwaltet werden können. Durch ein **Record** -Objekt kann auch eine Zeile in einem [Recordset](recordset-object-ado.md)-Objekt dargestellt werden, obwohl die Objekte **Record** und **Recordset** über unterschiedliche Methoden und Eigenschaften verfügen.

Das neue [Stream](stream-object-ado.md)-Objekt ermöglicht das Lesen, Schreiben und Verwalten des binären Byte- oder Textdatenstroms, aus dem ein Datei- oder Nachrichtendatenstrom besteht.

**[URL-Verwendung](absolute-and-relative-urls.md)**

In dieser Version wird außerdem die Verwendung von URLs (Uniform Resource Locators) als Alternative zu Verbindungszeichenfolgen und Befehlstext zum Benennen von Datenspeicherobjekten eingeführt. URLs können mit den vorhandenen Objekten [Connection](connection-object-ado.md) und **Recordset** sowie mit den neuen Objekten **Record** und **Stream** verwendet werden.

In dieser Version von ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* durch den auf das Windows 2000-Dateisystem zugegriffen wird, das vorhandene HTTP-Schema erkannt.

**[Spezielle Felder für Dokumentquellenanbieter](records-and-provider-supplied-fields.md)**

Eine spezielle Klasse von Anbietern von Anbietern von *Quelle des Dokuments* aufgerufen werden Ordner und Dokumente verwaltet. Wenn ein **Record** -Objekt ein Dokument stellt oder ein **Recordset** -Objekt einen Ordner von Dokumenten stellt, füllt der Dokumentquellenanbieter diese Objekte mit einem eindeutigen Satz von Feldern, die Merkmale des Dokuments beschrieben. Diese Felder bilden eine *Ressource* **oder ein **Recordset**** .

## <a name="new-reference-topics"></a>Neue Referenzthemen

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
<td><p><a href="charset-property-ado.md">CharSet</a></p></td>
<td><p>Der Zeichensatz wird angegeben, in den der Inhalt eines <strong>Stream</strong>-Textobjekts übersetzt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Gibt an, ob sich die aktuelle Position am Ende des Datenstroms befindet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Gibt das binäre Zeichen an, das als Zeilentrennzeichen in <strong>Stream</strong>-Textobjekten verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Zeigt die verfügbaren Berechtigungen zum Ändern von Daten in einem <strong>Connection</strong>-, <strong>Record</strong>- oder <strong>Stream</strong>-Objekt an.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Gibt die Zeichenfolge einer absoluten URL an, die auf das übergeordnete <strong>Record</strong>-Objekt des aktuellen <strong>Record</strong> -Objekts verweist.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Gibt die aktuelle Position in einem <strong>Stream</strong>-Objekt an.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Gibt den Typ des <strong>Record</strong>-Objekts an.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></p></td>
<td><p>Die Größe des Datenstroms wird als Byteanzahl angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Die Entität wird angegeben, die durch das <strong>Record</strong>-Objekt dargestellt wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt. Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Typ</a></p></td>
<td><p>Der Typ der im <strong>Stream</strong>-Objekt enthaltenen Daten (Binärdaten oder Textdaten) wird angegeben.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Kopiert die angegebene Anzahl von Zeichen oder Bytes (abhängig vom <strong>Typ</strong>) im <strong>Stream</strong> - <strong>Objekt</strong> in ein anderes <strong>Stream</strong> -Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Leeren</a></p></td>
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
<td><p><a href="open-method-ado-record.md">Open</a></p></td>
<td><p>Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
<td><p>Öffnet ein <strong>Stream</strong>-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Liest eine angegebene Anzahl von Bytes aus einem binären <strong>Stream</strong>-Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Liest eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Speichert den binären Inhalt eines <strong>Stream</strong>-Objekts in eine Datei.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Beim Lesen eines <strong>Stream</strong>-Textobjekts wird eine gesamte Zeile übersprungen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Schreiben</a></p></td>
<td><p>Schreibt Binärdaten in ein <strong>Stream</strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Schreibt eine angegebene Textzeichenfolge in ein <strong>Stream</strong>-Objekt.</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Neue und erweiterte Dokumentation

**[ADO-Codebeispiele](ado-code-examples.md)**

Die Beispiele wurden um in Microsoft Visual C++® und Microsoft Visual J++® geschriebene Codebeispiele erweitert. Sie können diese Codebeispiele kopieren und in den Editor einfügen.

**[Anhang A: Anbieter](appendix-a-providers.md)**

Es ist ein neues Thema enthalten, in dem die Verwendung von ADO mit dem [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) erläutert wird.

**[Programmieren mit ADO](appendix-c-programming-with-ado.md)**

Dieser neue Abschnitt enthält Tipps und Tricks für das Verwenden von ADO mit verschiedenen Programmiersprachen. Er enthält die vorhandenen Syntaxindizes für die Visual C++-Erweiterungen für ADO und ADO/WFC sowie neue Informationen speziell für Entwickler, die Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++ oder Microsoft Visual J++ verwenden.

