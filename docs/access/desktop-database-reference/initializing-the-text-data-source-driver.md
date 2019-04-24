---
title: Initialisieren des Text Datenquellentreibers
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291421"
---
# <a name="initializing-the-text-data-source-driver"></a>Initialisieren des Text Datenquellentreibers

**Gilt für**: Access 2013, Office 2013

Derselbe Datenbanktreiber wird sowohl für Textdatenquellen als auch für HTML-Datenquellen verwendet.

Wenn Sie den Datenquellentreiber der Text Datenbank installieren, schreibt das Setup Programm eine Reihe von Standardwerten in die Unterschlüssel Module und ISAM Formats in die Microsoft Windows-Registrierung. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.

## <a name="text-data-source-initialization-settings"></a>Initialisierungseinstellungen für Text Datenquellen

Der **Text Ordner Access\\Connectivity Engine\\ISAM Formats** enthält Initialisierungseinstellungen für den acetxt. dll-Treiber, der für den externen Zugriff auf Text Datendateien verwendet wird. Typical settings for the entries in this folder are shown in the following example.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

The Microsoft Access database engine uses the Text folder entries as follows.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eintrag</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Win32</p></td>
<td><p>Der Speicherort von Acetxt.dll. Der vollständige Pfad wird bei der Installation festgelegt. Die Werte sind vom Typ REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Die Anzahl der Zeilen, die beim Ermitteln des Spaltentyps geprüft werden. Mit dem Wert 0 wird die gesamte Datei durchsucht. Der Standardwert ist 25. Die Werte sind vom Typ REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Ein binärer Wert, der angibt, ob die erste Zeile der Tabelle Spaltennamen enthält. Der Wert 01 gibt an, dass beim Importieren die Spaltennamen aus der ersten Zeile verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Ein Indikator dazu, wie Textseiten gespeichert werden. Folgende Einstellungen sind möglich:</p>
<p></p>
<ul>
<li><p>ANSI: Die ANSI-Codepage des Computers. AnsiToUnicode- und UnicodeToAnsi-Konvertierungen werden durchgeführt.</p></li>
<li><p>OEM: Die OEM-Codepage des Computers. OemToUnicode- und UnicodeToOem-Konvertierungen werden durchgeführt.</p></li>
<li><p>Unicode: Es werden keine Codepagekonvertierungen durchgeführt.</p></li>
<li><p>&lt;Dezimalzahl&gt; – die Codepage-Nummer eines bestimmten Zeichensatzes. Konvertierungen von und nach Unicode werden durchgeführt.</p></li>
</ul>
<p></p>
<p>Der Standardwert ist ANSI. Die Werte sind vom Typ REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Format</p></td>
<td><p>Kann eine der folgenden sein: TabDelimited, CSVDelimited, Delimited (&lt;Single Character&gt;). Das einfarbige Trennzeichen im begrenzten Format kann ein beliebiges einzelnes Zeichen außer einem doppelten Anführungszeichen (&quot;) sein. Die Standardeinstellung ist CSVDelimited. Die Werte sind vom Typ REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Erweiterungen</p></td>
<td><p>Die Erweiterung von Dateinamen, die bei der Suche nach textbasierten Daten verwendet werden soll. Die Standardeinstellung ist txt, csv, tab, asc. Die Werte sind vom Typ REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Ein binärer Wert, der angibt, ob das entsprechende Währungssymbol beim Exportieren von Währungsfeldern eingeschlossen wird. Mit dem Wert 01 wird das Währungssymbol ebenfalls exportiert. Mit dem Wert 00 werden nur die numerischen Daten exportiert. Die Standardeinstellung ist 01. Die Werte sind vom Typ REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>Text Datenquellen-ISAM-Formate

Der **Text Ordner der\\Access Connectivity\\Engine-ISAM-Formate** enthält die folgenden Einträge.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Typ</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Modul</p></td>
<td><p>REG_SZ</p></td>
<td><p>Text</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Textdateien (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Textdateien (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="even">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>Isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Importiert Daten aus der externen Datei in die aktuelle Datenbank. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei nicht geändert.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Erstellt eine Tabelle in der aktuellen Datenbank, die mit der externen Datei verknüpft ist. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei geändert.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportiert Daten aus der aktuellen Datenbank in eine Textdatei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.

## <a name="html-import-isam-formats"></a>HTML-Import-ISAM-Formate

Der **HTML-Import\\Ordner "\\Access Connectivity Engine ISAM Formats** " enthält die folgenden Einträge.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Typ</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Modul</p></td>
<td><p>REG_SZ</p></td>
<td><p>Text</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML-Dateien (*. HT*)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>Isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Importiert Daten aus der externen Datei in die aktuelle Datenbank. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei nicht geändert.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Erstellt eine Tabelle in der aktuellen Datenbank, die mit der externen Datei verknüpft ist. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei geändert.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.

## <a name="html-export-isam-formats"></a>HTML-Export-ISAM-Formate

Der **HTML-Export\\Ordner "\\Access Connectivity Engine ISAM Formats** " enthält die folgenden Einträge.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Typ</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Modul</p></td>
<td><p>REG_SZ</p></td>
<td><p>Text</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML-Dateien (*.htm)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>Isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportiert Daten aus der aktuellen Datenbank in eine Textdatei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Anpassen der Datei "Schema. ini" für Text-und HTML-Daten

To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

Entsprechend sieht das Format für eine Datei mit Trennzeichen wie folgt aus:

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

Beim Exportieren von Daten in eine Textdatei mit Trennzeichen definieren Sie ebenfalls das Format für diese Datei:

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

Das Beispiel "My Special Export" bezieht sich auf eine spezielle Exportoption. Sie können beim Herstellen einer Verbindung beliebige Exportoptionen angeben. Im letzten Beispiel wird außerdem ein Datenquellenname (Data Source Name, DSN) verwendet, der beim Herstellen einer Verbindung wahlweise übergeben werden kann. Alle drei Formatabschnitte können in derselben INI-Datei vorhanden sein.

Das Microsoft Access-Datenbankmodul verwendet die Einträge in der Datei Schema.ini wie folgt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eintrag</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>Mögliche Werte sind <strong>True</strong> (der erste Datensatz bezeichnet die Spaltennamen) oder <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Format</p></td>
<td><p>Kann auf einen der folgenden Werte festgelegt werden: TabDelimited, CSVDelimited, Delimited&lt;(einzelnes&gt;Zeichen) oder FixedLength. Das für das Dateiformat mit Trennzeichen angegebene Delimiter kann ein beliebiges, außer einem doppelten Anführungszeichen (&quot;) sein.</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Diese Option wird nur für das Format FixedLength verwendet und kann einen der folgenden Werte aufweisen: RaggedEdge oder TrueFixedLength. Mit RaggedEdge können Zeilen mit einem Wagenrücklaufzeichen beendet werden. Mit TrueFixedLength muss jede Zeile eine ganz bestimmte Anzahl von Zeichen enthalten, und alle Wagenrücklaufzeichen, die sich nicht am Zeilenende befinden, werden als in ein Feld eingebettet interpretiert. Wenn diese Einstellung nicht vorhanden ist, wird der Standardwert RaggedEdge verwendet.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Gibt die Anzahl der Zeilen an, die beim Ermitteln des Spaltentyps geprüft werden. Mit dem Wert 0 wird die gesamte Datei durchsucht.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Mögliche Werte sind OEM, ANSI, UNICODE oder die Dezimalzahl einer gültigen Codepage. Gibt den Zeichensatz der Quelldatei an.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Hiermit wird die Formatzeichenfolge für Datums- und Uhrzeitangaben festgelegt. Dieser Eintrag muss angegeben werden, wenn für alle Datums-/Uhrzeitfelder beim Importieren/Exportieren dasselbe Format verwendet werden soll. Alle Microsoft Jet-Datenbankmodul-Formate außer AM und PM werden unterstützt. Wenn keine Formatzeichenfolge vorhanden ist, werden das kurze Datumsformat und das Zeitformat der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Gibt das Währungssymbol an, das in der Textdatei für Währungswerte verwendet werden soll. Beispiele hierfür sind das Dollarzeichen ($) und das Eurozeichen (€). Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Kann auf einen der folgenden Werte festgelegt werden: Währungssymbolpräfix ohne Trennung ($1) Währungssymbolsuffix ohne Trennung ($1) Währungssymbolpräfix mit einem Zeichenabstand ($1) Währungssymbolsuffix mit einer Zeichen Trennung ($1), wenn dieser Eintrag abwesend ist, wird der Standardwert in der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Gibt die Anzahl der Kommastellen eines Währungsbetrags an. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Kann einer der folgenden Werte sein: ($1) – $1 $ – $1 1 – ($1) – $1 1 – $1 $ – – $1 – $1 $1 – $1 – $ – 1 1 – $ ($1) ($1) das Dollarzeichen wird für die Zwecke dieses Beispiels angezeigt, aber es sollte durch den entsprechenden CurrencySymbol-Wert im tatsächlichen Programm ersetzt werden. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Gibt das aus einem einzelnen Zeichen bestehende Symbol an, das in der Textdatei zum Trennen der Tausenderstellen von Währungswerten verwendet werden soll. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Hierfür kann ein beliebiges einzelnes Zeichen verwendet werden, mit dem die Tausenderstellen von den Kommastellen eines Währungsbetrags getrennt werden. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Hierfür kann ein beliebiges einzelnes Zeichen verwendet werden, mit dem die ganze Zahl von den Kommastellen einer Zahl getrennt werden. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Gibt die Anzahl der Kommastellen einer Zahl an. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Gibt an, ob ein Dezimalwert, der kleiner als 1 und größer als –1 ist, führende Nullen enthalten soll. Mögliche Werte sind False (keine führende Nullen) oder True.</p></td>
</tr>
<tr class="even">
<td><p>Col1, col2,...</p></td>
<td><p>Die in der Textdatei zu lesenden Spalten. Das Format dieses Eintrags sollte sein: <em>coln</em>=<em>ColumnName</em> Type [Width <em> #</em>] <em>ColumnName</em>: Spaltennamen mit eingebetteten Leerzeichen sollten in Anführungszeichen eingeschlossen werden. <em>Typ</em>: kann Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime sein. Binary, OLE, Text oder Memo. Darüber hinaus werden die folgenden ODBC-Text Treibertypen unterstützt: char (identisch mit Text) float (identisch mit Double) Integer (identisch mit Short) LongChar (identisch mit Memo) Datums <em>Format</em> im Fall eines Memo Typs eine zusätzliche Formatmarkierung [Attribut Hyperlink] wird verwendet, um Spalten anzugeben, die aktive URLs in Microsoft Access sein sollen. Beim Typ Decimal müssen die zusätzlichen Formatmarkierungen [Scale #] Precision #] verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>Texttrenner</p></td>
<td><p>Hierfür kann jedes beliebige einzelne Zeichen zum Trennen von Zeichenfolgen verwendet werden, die eines der anderen Sonderzeichen enthalten. Beispiel: &quot;ABC&quot;,&quot;XYZ, PQR&quot;,&quot;hij&quot; wenn dieser Eintrag nicht vorhanden ist, ist das Standardtrennzeichen ein doppeltes Anführungszeichen. Wenn dieser Eintrag die Zeichenfolge &quot;None&quot; ist, werden keine Zeichen als Begrenzer behandelt.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.


