---
title: Initialisieren des Text-Datenquellentreibers
TOCTitle: Initializing the Text Data Source Driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb897c4e057b767c98676bc14c9f1e70c22095ee
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474859"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="5fb15-102">Initialisieren des Text-Datenquellentreibers</span><span class="sxs-lookup"><span data-stu-id="5fb15-102">Initializing the Text Data Source Driver</span></span>


<span data-ttu-id="5fb15-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fb15-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="5fb15-104">Für Text- und HTML-Datenquellen wird derselben Datenbanktreiber verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-104">The same database driver is used for both Text Data sources and for HTML data sources.</span></span>

<span data-ttu-id="5fb15-p101">Beim Installieren des Textdatenquellen-Datenbanktreibers schreibt das Setupprogramm Standardwerte in die Unterschlüssel Engines und ISAM Formats der Microsoft® Windows®-Registrierung. Diese Einstellungen dürfen nicht direkt geändert werden. Verwenden Sie stattdessen das Setupprogramm, um diese Einstellungen hinzuzufügen, zu entfernen oder zu ändern. In den folgenden Abschnitten werden die Einstellungen für die Initialisierung und das ISAM-Format für den Textdatenquellen-Datenbanktreiber beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p101">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft® Windows® Registry in the Engines and ISAM Formats subkeys. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="5fb15-108">Initialisierungseinstellungen für Textdatenquellen</span><span class="sxs-lookup"><span data-stu-id="5fb15-108">Text Data Source Initialization Settings</span></span>

<span data-ttu-id="5fb15-109">Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\Ordner Text** enthält initialisierungseinstellungen für Acetxt.dll-Treiber für den externen Zugriff auf Daten Textdateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="5fb15-110">Standardeinstellungen für die Einträge in diesem Ordner sind im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<span data-ttu-id="5fb15-111">Das Microsoft Access-Datenbankmodul verwendet die Einträge im Ordner Text wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fb15-112">Eintrag</span><span class="sxs-lookup"><span data-stu-id="5fb15-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="5fb15-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fb15-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-114">Win32</span><span class="sxs-lookup"><span data-stu-id="5fb15-114">win32</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p103">Der Speicherort von Acetxt.dll. Der vollständige Pfad wird bei der Installation festgelegt. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p103">The location of Acetxt.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="5fb15-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p104">Die Anzahl der Zeilen, die beim Ermitteln des Spaltentyps geprüft werden. Mit dem Wert 0 wird die gesamte Datei durchsucht. Der Standardwert ist 25. Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p104">The number of rows to be scanned when guessing the column types. If set to 0, the entire file will be searched. The default is 25. Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="5fb15-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p105">Ein binärer Wert, der angibt, ob die erste Zeile der Tabelle Spaltennamen enthält. Der Wert 01 gibt an, dass beim Importieren die Spaltennamen aus der ersten Zeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p105">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-126">UTF</span><span class="sxs-lookup"><span data-stu-id="5fb15-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p106">Ein Indikator dazu, wie Textseiten gespeichert werden. Folgende Einstellungen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="5fb15-p106">An indicator of how text pages are stored. Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="5fb15-p107">ANSI: Die ANSI-Codepage des Computers. AnsiToUnicode- und UnicodeToAnsi-Konvertierungen werden durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p107">ANSI — The ANSI code page of the machine. AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="5fb15-p108">OEM: Die OEM-Codepage des Computers. OemToUnicode- und UnicodeToOem-Konvertierungen werden durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p108">OEM — The OEM code page of the machine. OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="5fb15-133">Unicode: Es werden keine Codepagekonvertierungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="5fb15-134">&lt;Dezimalzahl&gt; – die Seitenzahl Code, der einen bestimmten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="5fb15-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="5fb15-135">In und aus Unicode konvertiert werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="5fb15-p110">Der Standardwert ist ANSI. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p110">The default is ANSI. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-138">Format</span><span class="sxs-lookup"><span data-stu-id="5fb15-138">Format</span></span></p></td>
<td><p><span data-ttu-id="5fb15-139">Kann eine der folgenden sein: TabDelimited, CSVDelimited, mit Trennzeichen (&lt;einzelnes Zeichen&gt;).</span><span class="sxs-lookup"><span data-stu-id="5fb15-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="5fb15-140">Einzelnes Zeichen als Trennzeichen in das Format mit Trennzeichen kann ein beliebiges einzelnes Zeichen außer doppelte Anführungszeichen (&quot;).</span><span class="sxs-lookup"><span data-stu-id="5fb15-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="5fb15-141">Der Standardwert ist CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="5fb15-141">The default is CSVDelimited.</span></span> <span data-ttu-id="5fb15-142">Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="5fb15-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-143">Extensions</span><span class="sxs-lookup"><span data-stu-id="5fb15-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p112">Die Erweiterung von Dateinamen, die bei der Suche nach textbasierten Daten verwendet werden soll. Die Standardeinstellung ist txt, csv, tab, asc. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p112">The extension of any files to be browsed when looking for text-based data. The default is txt, csv, tab, asc. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="5fb15-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p113">Ein binärer Wert, der angibt, ob das entsprechende Währungssymbol beim Exportieren von Währungsfeldern eingeschlossen wird. Mit dem Wert 01 wird das Währungssymbol ebenfalls exportiert. Mit dem Wert 00 werden nur die numerischen Daten exportiert. Die Standardeinstellung ist 01. Die Werte sind vom Typ REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p113">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported. A value of 01 indicates that the symbol is included. A value of 00 indicates that only the numeric data is exported. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="5fb15-153">Textdatenquellen-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="5fb15-153">Text Data Source ISAM Formats</span></span>

<span data-ttu-id="5fb15-154">Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\Text** Ordner enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="5fb15-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fb15-155">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="5fb15-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="5fb15-156">Type</span><span class="sxs-lookup"><span data-stu-id="5fb15-156">Type</span></span></p></th>
<th><p><span data-ttu-id="5fb15-157">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb15-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-158">Engine</span><span class="sxs-lookup"><span data-stu-id="5fb15-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="5fb15-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-160">Text</span><span class="sxs-lookup"><span data-stu-id="5fb15-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="5fb15-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="5fb15-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-163">Textdateien (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="5fb15-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="5fb15-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="5fb15-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-166">Textdateien (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="5fb15-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="5fb15-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="5fb15-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-169">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="5fb15-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="5fb15-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-172">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="5fb15-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="5fb15-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="5fb15-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="5fb15-175">2</span><span class="sxs-lookup"><span data-stu-id="5fb15-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="5fb15-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="5fb15-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-178">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="5fb15-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-181">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="5fb15-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p114">Importiert Daten aus der externen Datei in die aktuelle Datenbank. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p114">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="5fb15-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="5fb15-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p115">Erstellt eine Tabelle in der aktuellen Datenbank, die mit der externen Datei verknüpft ist. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei geändert.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p115">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="5fb15-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p116">Exportiert Daten aus der aktuellen Datenbank in eine Textdatei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p116">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="5fb15-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="5fb15-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-196">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-196">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="5fb15-197">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span></P>



## <a name="html-import-isam-formats"></a><span data-ttu-id="5fb15-198">HTML-Import-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="5fb15-198">HTML Import ISAM Formats</span></span>

<span data-ttu-id="5fb15-199">Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\HTML-Import** Ordner enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="5fb15-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fb15-200">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="5fb15-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="5fb15-201">Type</span><span class="sxs-lookup"><span data-stu-id="5fb15-201">Type</span></span></p></th>
<th><p><span data-ttu-id="5fb15-202">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb15-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-203">Engine</span><span class="sxs-lookup"><span data-stu-id="5fb15-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="5fb15-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-205">Text</span><span class="sxs-lookup"><span data-stu-id="5fb15-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="5fb15-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="5fb15-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-208">HTML-Dateien (\*.HT \*\*)</span><span class="sxs-lookup"><span data-stu-id="5fb15-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="5fb15-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="5fb15-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-211">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="5fb15-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="5fb15-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-214">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="5fb15-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="5fb15-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="5fb15-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="5fb15-217">2</span><span class="sxs-lookup"><span data-stu-id="5fb15-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="5fb15-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="5fb15-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-220">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="5fb15-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-223">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="5fb15-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p117">Importiert Daten aus der externen Datei in die aktuelle Datenbank. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p117">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="5fb15-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="5fb15-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p118">Erstellt eine Tabelle in der aktuellen Datenbank, die mit der externen Datei verknüpft ist. Durch das Ändern von Daten in der aktuellen Datenbank werden die Daten in der externen Datei geändert.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p118">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="5fb15-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="5fb15-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-234">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-234">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="5fb15-235">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span></P>



## <a name="html-export-isam-formats"></a><span data-ttu-id="5fb15-236">HTML-Export-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="5fb15-236">HTML Export ISAM Formats</span></span>

<span data-ttu-id="5fb15-237">Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\HTML-Export** Ordner enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="5fb15-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fb15-238">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="5fb15-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="5fb15-239">Type</span><span class="sxs-lookup"><span data-stu-id="5fb15-239">Type</span></span></p></th>
<th><p><span data-ttu-id="5fb15-240">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb15-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-241">Engine</span><span class="sxs-lookup"><span data-stu-id="5fb15-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="5fb15-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-243">Text</span><span class="sxs-lookup"><span data-stu-id="5fb15-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="5fb15-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="5fb15-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-246">HTML-Dateien (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="5fb15-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="5fb15-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="5fb15-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-249">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="5fb15-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="5fb15-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-252">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="5fb15-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="5fb15-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="5fb15-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="5fb15-255">2</span><span class="sxs-lookup"><span data-stu-id="5fb15-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="5fb15-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="5fb15-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-258">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="5fb15-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-261">00</span><span class="sxs-lookup"><span data-stu-id="5fb15-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="5fb15-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="5fb15-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5fb15-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p119">Exportiert Daten aus der aktuellen Datenbank in eine Textdatei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p119">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="5fb15-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="5fb15-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fb15-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5fb15-268">01</span><span class="sxs-lookup"><span data-stu-id="5fb15-268">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="5fb15-269">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span></P>



## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="5fb15-270">Anpassen der Datei "Schema.ini" für Text- und HTML-Daten</span><span class="sxs-lookup"><span data-stu-id="5fb15-270">Customizing the Schema.ini File for Text and HTML Data</span></span>

<span data-ttu-id="5fb15-p120">Zum Lesen, Importieren oder Exportieren von Text- und HTML-Daten müssen Sie die Datei Schema.ini erstellen und die Text-ISAM-Informationen in die INI-Datei eingeben. Schema.ini enthält Angaben zur Datenquelle: wie der Text formatiert wird, wie er beim Importieren gelesen wird und welches Standardexportformat für Dateien verwendet wird. Im folgenden Beispiel ist das Layout für Filename.txt, eine Datei fester Breite, dargestellt:</span><span class="sxs-lookup"><span data-stu-id="5fb15-p120">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

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

<span data-ttu-id="5fb15-274">Entsprechend sieht das Format für eine Datei mit Trennzeichen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="5fb15-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<span data-ttu-id="5fb15-275">Beim Exportieren von Daten in eine Textdatei mit Trennzeichen definieren Sie ebenfalls das Format für diese Datei:</span><span class="sxs-lookup"><span data-stu-id="5fb15-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

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

<span data-ttu-id="5fb15-p121">Das Beispiel "My Special Export" bezieht sich auf eine spezielle Exportoption. Sie können beim Herstellen einer Verbindung beliebige Exportoptionen angeben. Im letzten Beispiel wird außerdem ein Datenquellenname (Data Source Name, DSN) verwendet, der beim Herstellen einer Verbindung wahlweise übergeben werden kann. Alle drei Formatabschnitte können in derselben INI-Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p121">The My Special Export example refers to a specific export option; you can specify any variation of export options at connect time. This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time. All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="5fb15-279">Das Microsoft Access-Datenbankmodul verwendet die Einträge in der Datei Schema.ini wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5fb15-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fb15-280">Eintrag</span><span class="sxs-lookup"><span data-stu-id="5fb15-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="5fb15-281">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fb15-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="5fb15-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="5fb15-283">Mögliche Werte sind <strong>True</strong> (der erste Datensatz bezeichnet die Spaltennamen) oder <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fb15-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-284">Format</span><span class="sxs-lookup"><span data-stu-id="5fb15-284">Format</span></span></p></td>
<td><p><span data-ttu-id="5fb15-285">Kann auf einen der folgenden Werte festgelegt werden: TabDelimited, CSVDelimited, mit Trennzeichen (&lt;einzelnes Zeichen&gt;), oder FixedLength.</span><span class="sxs-lookup"><span data-stu-id="5fb15-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="5fb15-286">Das Trennzeichen für das Dateiformat mit Trennzeichen ein beliebiges einzelnes Zeichen außer doppelte Anführungszeichen werden kann (&quot;).</span><span class="sxs-lookup"><span data-stu-id="5fb15-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="5fb15-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="5fb15-288">Diese Option wird nur für das Format FixedLength verwendet und kann einen der folgenden Werte aufweisen: RaggedEdge oder TrueFixedLength.
</span><span class="sxs-lookup"><span data-stu-id="5fb15-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="5fb15-289">Mit RaggedEdge können Zeilen mit einem Wagenrücklaufzeichen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="5fb15-290">Mit TrueFixedLength muss jede Zeile eine ganz bestimmte Anzahl von Zeichen enthalten, und alle Wagenrücklaufzeichen, die sich nicht am Zeilenende befinden, werden als in ein Feld eingebettet interpretiert.</span><span class="sxs-lookup"><span data-stu-id="5fb15-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="5fb15-291">Wenn diese Einstellung nicht vorhanden ist, wird der Standardwert RaggedEdge verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="5fb15-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p124">Gibt die Anzahl der Zeilen an, die beim Ermitteln des Spaltentyps geprüft werden. Mit dem Wert 0 wird die gesamte Datei durchsucht.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p124">Indicates the number of rows to be scanned when guessing the column data types. If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-295">UTF</span><span class="sxs-lookup"><span data-stu-id="5fb15-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="5fb15-296">Mögliche Werte sind OEM, ANSI, UNICODE oder die Dezimalzahl einer gültigen Codepage. Gibt den Zeichensatz der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="5fb15-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5fb15-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p125">Hiermit wird die Formatzeichenfolge für Datums- und Uhrzeitangaben festgelegt. Dieser Eintrag muss angegeben werden, wenn für alle Datums-/Uhrzeitfelder beim Importieren/Exportieren dasselbe Format verwendet werden soll. Alle Microsoft Jet-Datenbankmodul-Formate außer AM und PM werden unterstützt. Wenn keine Formatzeichenfolge vorhanden ist, werden das kurze Datumsformat und das Zeitformat der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p125">Can be set to a format string indicating dates and times. This entry should be specified if all date/time fields in the import/export are handled with the same format. All of the Microsoft Jet database engine formats except AM and PM are supported. In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="5fb15-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p126">Gibt das Währungssymbol an, das in der Textdatei für Währungswerte verwendet werden soll. Beispiele hierfür sind das Dollarzeichen ($) und das Eurozeichen (€). Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p126">Indicates the currency symbol to be used for currency values in the text file. Examples include the dollar sign ($) and Dm. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="5fb15-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="5fb15-307">Kann auf einen der folgenden Werte festgelegt werden: mit kein Trennung ($1) Währung Symbol Suffix mit keine Trennung (1$) mit einem Zeichen voneinander getrennt zu halten ($ 1) Währung Symbol Suffix Währungssymbolpräfix mit einem Leerzeichen (1 $) Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert in der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="5fb15-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p127">Gibt die Anzahl der Kommastellen eines Währungsbetrags an. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p127">Specifies the number of digits used for the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="5fb15-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="5fb15-312">Kann eine der folgenden Werte sein: ($1) – $1 – 1 $ $1 – (1$) – 1$ 1 – 1$ $– – 1 $ – $ 1-1 $– $ 1 – $-1-1 – $ ($ 1) (1 $) wird das Dollarzeichen aus Gründen der in diesem Beispiel wird gezeigt, aber mit den entsprechenden CurrencySymbol-Wert in die tatsächliche Anwendung ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5fb15-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="5fb15-313">Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="5fb15-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p129">Gibt das aus einem einzelnen Zeichen bestehende Symbol an, das in der Textdatei zum Trennen der Tausenderstellen von Währungswerten verwendet werden soll. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p129">Indicates the single-character symbol to be used for separating currency values by thousands in the text file. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="5fb15-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p130">Hierfür kann ein beliebiges einzelnes Zeichen verwendet werden, mit dem die Tausenderstellen von den Kommastellen eines Währungsbetrags getrennt werden. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p130">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="5fb15-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p131">Hierfür kann ein beliebiges einzelnes Zeichen verwendet werden, mit dem die ganze Zahl von den Kommastellen einer Zahl getrennt werden. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p131">Can be set to any single character that is used to separate the integer from the fractional part of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="5fb15-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="5fb15-p132">Gibt die Anzahl der Kommastellen einer Zahl an. Wenn dieser Eintrag nicht vorhanden ist, wird der Standardwert aus der Windows-Systemsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb15-p132">Indicates the number of decimal digits in the fractional portion of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="5fb15-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="5fb15-327">Gibt an, ob ein Dezimalwert, der kleiner als 1 und größer als –1 ist, führende Nullen enthalten soll. Mögliche Werte sind False (keine führende Nullen) oder True.</span><span class="sxs-lookup"><span data-stu-id="5fb15-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb15-328">Col1, Col2, …</span><span class="sxs-lookup"><span data-stu-id="5fb15-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="5fb15-329">Listet die Spalten in der Textdatei gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5fb15-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="5fb15-330">Das Format dieses Eintrags werden sollten: <em>Spalte</em>=<em>Spaltenname</em> Typ [Width <em> #</em>] <em>Spaltenname</em>: Spaltennamen mit eingebetteten Leerzeichen in Anführungszeichen eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fb15-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="5fb15-331"><em>Typ</em>: kann Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="5fb15-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="5fb15-332">Binary, OLE, Text oder Memo.</span><span class="sxs-lookup"><span data-stu-id="5fb15-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="5fb15-333">Darüber hinaus werden die folgenden ODBC-Texttreibertypen unterstützt: Char (identisch mit Text) Float (identisch mit Double) Integer (identisch mit Short) LongChar (identisch mit Memo) Date <em>Datumsformat</em> beim Typ Memo eine zusätzliche Format Markierung [Attribute Hyperlink kann] verwendet, um Spalten angeben, die in Microsoft Access aktive URLs sein sollte.</span><span class="sxs-lookup"><span data-stu-id="5fb15-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="5fb15-334">Beim Typ Decimal müssen die zusätzlichen Formatmarkierungen [Scale #] Precision #] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb15-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="5fb15-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="5fb15-336">Hierfür kann jedes beliebige einzelne Zeichen zum Trennen von Zeichenfolgen verwendet werden, die eines der anderen Sonderzeichen enthalten.
</span><span class="sxs-lookup"><span data-stu-id="5fb15-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="5fb15-337">E.g.</span><span class="sxs-lookup"><span data-stu-id="5fb15-337">E.g.</span></span> <span data-ttu-id="5fb15-338">&quot;ABC&quot;,&quot;Xyz Pqr&quot;,&quot;Hij&quot; Wenn dieser Eintrag nicht vorhanden ist, werden das Standardtrennzeichen doppelte Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="5fb15-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="5fb15-339">Wenn dieser Eintrag die Zeichenfolge ist &quot;keine&quot; und keines der Zeichen als Trennzeichen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5fb15-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="5fb15-340">Wenn Sie Einstellungen in der Datei Schema.ini ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="5fb15-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


