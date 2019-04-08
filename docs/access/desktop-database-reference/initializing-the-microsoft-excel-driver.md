---
title: Initialisieren des Microsoft Excel-Treibers
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: e59070b67358b3700ca677149a849768c144c1a3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2019
ms.locfileid: "31518131"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Initialisieren des Microsoft Excel-Treibers

**Gilt für**: Excel 2016 | Zugriff 2016 | Zugriff 2013 | Office 2013 | Excel 2013 | Office for Business-Zugriff 2013 | Excel 2010 | Access 2010

Wenn Sie den Excel-Treiber installieren, schreibt das Setup Programm in der Unterschlüssel Engines-und ISAM-Formate in der Windows-Registrierung eine Reihe von Standardwerten. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.

## <a name="excel-initialization-settings"></a>Excel-Initialisierungseinstellungen

Der **Excel-Ordner\\Access\\Connectivity Engine Engines** enthält Initialisierungseinstellungen für den Aceexcl. dll-Treiber, der für den externen Zugriff auf Microsoft Excel-Arbeitsblätter verwendet wird. Typical settings for the entries in this folder are shown in the following example.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

The Microsoft Access database engine uses the Excel folder entries as follows.

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
<td><p>Der Speicherort von msexcl40.dll. Der vollständige Pfad wird bei der Installation festgelegt. Die Werte sind vom Typ REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Die Anzahl der Zeilen, die für den Datentyp überprüft werden sollen. Der Datentyp wird anhand der maximalen Anzahl von Datentypen ermittelt. Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt: Number, Currency, Date, Text, Boolean. Wenn Daten gefunden werden, die nicht mit dem für die Spalte erkannten Datentyp übereinstimmen, wird er als <strong>null</strong> -Wert zurückgegeben. Wenn eine Spalte beim Importieren gemischte Datentypen enthält, wird die gesamte Spalte gemäß der ImportMixedTypes-Einstellung umgewandelt. Standardmäßig werden 8 Zeilen geprüft. Die Werte sind vom Typ REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Mögliche Werte sind MajorityType und Text. Mit MajorityType werden Spalten mit gemischten Datentypen beim Importieren in den vorherrschenden Datentyp konvertiert. Mit Text werden Spalten mit gemischten Datentypen beim Importieren in Text konvertiert. Die Standardeinstellung ist Text. Die Werte sind vom Typ REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>Die Anzahl leerer Zeichen, die vor neuen Daten am Ende eines Arbeitsblatts der Version 3.5 oder Version 4.0 eingefügt werden. Wenn AppendBlankRows beispielsweise auf 4 festgelegt wird, fügt Microsoft Jet 4 leere Zeilen am Ende des Arbeitsblatts ein, und danach erst Zeilen mit Daten. Mögliche ganzzahlige Werte für diese Einstellungen sind die Zahlen 0 bis 16; die Standardeinstellung ist 01 (eine zusätzliche Zeile wird eingefügt). Die Werte sind vom Typ REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Ein binärer Wert, der angibt, ob die erste Zeile der Tabelle Spaltennamen enthält. Der Wert 01 gibt an, dass beim Importieren die Spaltennamen aus der ersten Zeile verwendet werden. Der Wert 00 gibt an, dass in der ersten Zeile keine Spaltennamen verwendet werden; Spaltennamen werden als F1, F2, F3 usw. angezeigt. Die Standardeinstellung ist 01. Die Werte sind vom Typ REG_BINARY.</p></td>
</tr>
</tbody>
</table>

<br/>

Der Ordner **Access Connectivity\\Engine\\Engines Excel 8,0** enthält die folgenden einträge, die für Microsoft Excel 97 gelten.

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
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
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
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportiert Daten aus der aktuellen Datenbank in eine Microsoft Excel 97-Datei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Verwenden der TypeGuessRows-Einstellung für den Excel-Treiber
Bei Verwendung des Microsoft Excel-Treibers können Sie mit dem **TypeGuessRows** -Registrierungswert konfigurieren, wie viele Zeilen für den Datentyp überprüft werden sollen. Der **TypeGuessRows** -Wert befindet sich unter dem folgenden Registrierungsschlüssel:

# [<a name="office-2016"></a>Office 2016](#tab/office-2016)

Für eine MSI-Installation von Office

- Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access-Engine\Engines\Excel**

- Für 32-Bit-Office unter 64-Bit-Windows:

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access-Engine\Engines\Excel**
    
Für eine Klick-und-Los-Installation von Office

- Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access-Engine\Engines\Excel**

- Für 32-Bit-Office unter 64-Bit-Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access-Engine\Engines\Excel**

Die standardmäßige Anzahl der zu überprüfenden Zeilen ist **8** (acht). Wenn Sie den **TypeGuessRows** -Wert auf **0** (null) festlegen, überprüft der Excel-Treiber die ersten 16.384-Zeilen nach dem Datentyp. Wenn Sie mehr als 16.384 Zeilen überprüfen möchten, legen Sie **TypeGuessRows** auf einen Wert fest, der auf Ihrem gewünschten Range basiert. Legen Sie **TypeGuessRows** auf 1.048.576 (die maximale Anzahl von Zeilen, die in Excel zulässig sind) fest, um alle Zeilen zu überprüfen.
 
Der Datentyp wird durch die maximale Anzahl von Datentypen bestimmt, die gefunden werden. Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt:

- Zahl
- Währung
- Datum
- Text
- Boolesch

Wenn Daten gefunden werden, die nicht mit dem geschätzten Datentyp für die Spalte übereinstimmen, werden diese Daten als **null** -Wert zurückgegeben. Wenn während eines Imports eine Spalte gemischte Datentypen enthält, wird die gesamte Spalte in den Datentyp umgewandelt, der von der **ImportMixedTypes** -Einstellung festgelegt wird.

# [<a name="office-2013"></a>Office 2013](#tab/office-2013)

Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access-Engine\Engines\Excel**

Für 32-Bit-Office unter 64-Bit-Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access-Engine\Engines\Excel**

Die standardmäßige Anzahl der zu überprüfenden Zeilen ist **8** (acht). Wenn Sie den **TypeGuessRows** -Wert auf **0** (null) festlegen, überprüft der Excel-Treiber die ersten 16.384-Zeilen nach dem Datentyp. Wenn Sie mehr als 16.384 Zeilen überprüfen möchten, legen Sie **TypeGuessRows** auf einen Wert fest, der auf Ihrem gewünschten Range basiert. Legen Sie **TypeGuessRows** auf 1.048.576 (die maximale Anzahl von Zeilen, die in Excel zulässig sind) fest, um alle Zeilen zu überprüfen.
 
Der Datentyp wird durch die maximale Anzahl von Datentypen bestimmt, die gefunden werden. Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt:

- Zahl
- Währung
- Datum
- Text
- Boolesch

Wenn Daten gefunden werden, die nicht mit dem geschätzten Datentyp für die Spalte übereinstimmen, werden diese Daten als **null** -Wert zurückgegeben. Wenn während eines Imports eine Spalte gemischte Datentypen enthält, wird die gesamte Spalte in den Datentyp umgewandelt, der von der **ImportMixedTypes** -Einstellung festgelegt wird.

# [<a name="office-2010"></a>Office 2010](#tab/office-2010)

Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access-Engine\Engines\Excel**

Für 32-Bit-Office unter 64-Bit-Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access-Engine\Engines\Excel**

Die standardmäßige Anzahl der zu überprüfenden Zeilen ist **8** (acht). Wenn Sie den **TypeGuessRows** -Wert auf **0** (null) festlegen, überprüft der Excel-Treiber die ersten 16.384-Zeilen nach dem Datentyp. Wenn Sie mehr als 16.384 Zeilen überprüfen möchten, legen Sie **TypeGuessRows** auf einen Wert fest, der auf Ihrem gewünschten Range basiert. Legen Sie **TypeGuessRows** auf 1.048.576 (die maximale Anzahl von Zeilen, die in Excel zulässig sind) fest, um alle Zeilen zu überprüfen.
 
Der Datentyp wird durch die maximale Anzahl von Datentypen bestimmt, die gefunden werden. Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt:

- Zahl
- Währung
- Datum
- Text
- Boolesch

Wenn Daten gefunden werden, die nicht mit dem geschätzten Datentyp für die Spalte übereinstimmen, werden diese Daten als **null** -Wert zurückgegeben. Wenn während eines Imports eine Spalte gemischte Datentypen enthält, wird die gesamte Spalte in den Datentyp umgewandelt, der von der **ImportMixedTypes** -Einstellung festgelegt wird.

---
> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.

## <a name="see-also"></a>Siehe auch

- [Verwenden der TypeGuessRows-Einstellung für den Excel-Treiber](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

