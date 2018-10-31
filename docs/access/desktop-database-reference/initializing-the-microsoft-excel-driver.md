---
title: Initialisieren des Microsoft Excel-Treibers
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 85961b761255583738026113a025d6ca84b61f83
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861988"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Initialisieren des Microsoft Excel-Treibers

**Betrifft**: Access 2013 | Office 2013

Bei der Installation des Excel-Treibers schreibt das Setupprogramm Standardwerte der Windows-Registrierung im Unterschlüssel Module und -ISAM-Formate. Sie sollten diese Einstellungen nicht direkt geändert. Verwenden Sie das Setupprogramm für Ihre Anwendung hinzufügen, entfernen oder ändern Sie diese Einstellung. In den folgenden Abschnitten werden die Initialisierung und ISAM formateinstellungen für die Microsoft Excel-Datenbanktreibers beschrieben.

## <a name="excel-initialization-settings"></a>Initialisierungseinstellungen für Excel

Die **Konnektivitätsmodul für Access\\Module\\Excel** Ordner enthält initialisierungseinstellungen für Aceexcl.dll-Treiber für den externen Zugriff zu Microsoft Excel-Arbeitsblättern verwendet. Standardeinstellungen für die Einträge in diesem Ordner sind im folgenden Beispiel dargestellt.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

Das Microsoft Access-Datenbankmodul verwendet die Einträge im Ordner Excel wie folgt.

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
<td><p>Die Anzahl der Zeilen für den Datentyp überprüft werden soll. Der Datentyp ist die maximale Anzahl von Arten von Daten anhand. Wenn eine Tie vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt: Zahl, Währung, Datum, Text, Boolean. Wenn Daten, die nicht den Datentyp für die Spalte ermittelten übereinstimmt gefunden werden, wird es als einen <strong>Null</strong> -Wert zurückgegeben. Beim Import Wenn eine Spalte gemischte Datentypen wurde wird die gesamte Spalte gemäß der ImportMixedTypes-Einstellung umgewandelt werden. Die Standardanzahl von Zeilen zu überprüfenden ist 8. Die Werte sind vom Typ REG_DWORD.</p></td>
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


Die **Konnektivitätsmodul für Access\\Module\\Excel 8.0** Ordner enthält die folgenden Einträge, die für Microsoft Excel 97 gelten.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Type</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
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
<td><p>IsamType</p></td>
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


> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.

## <a name="see-also"></a>Siehe auch

[Verwenden die Einstellung TypeGuessRows für Excel-Treibers](https://support.office.com/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b)
