---
title: ImportExportSpreadsheet-Makroaktion
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 06d633cac926015aab985420a618005d8c6774b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612050"
---
# <a name="importexportspreadsheet-macro-action"></a>ImportExportSpreadsheet-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **ImportExportSpreadsheet** -Aktion können Sie Daten zwischen der aktuellen Access-Datenbank (.mdb oder .accdb) oder einem Access-Projekt (.adp) und einer Tabellenkalkulationsdatei importieren oder exportieren. Sie können auch die Daten in einer Microsoft Excel-Tabellenkalkulation mit der aktuellen Microsoft Access-Datenbank verknüpfen. Bei einer verknüpften Tabellenkalkulation können Sie die Tabellenkalkulationsdaten mit Access anzeigen und bearbeiten, während trotzdem uneingeschränkter Zugriff auf die Daten aus Ihrem Excel-Tabellenkalkulationsprogramm möglich ist. Sie können auch eine Verknüpfung mit Daten in einer Lotus-1-2-3-Tabellenkalkulationsdatei herstellen, diese Daten sind jedoch in Access schreibgeschützt. .

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **TransferSpreadsheet**-Aktion verwendet die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Transfertyp</strong></p></td>
<td><p>Der Transfertyp, den Sie vornehmen möchten. Wählen Sie <strong>Importieren</strong>, <strong>Exportieren</strong> oder <strong>Verknüpfen</strong> im Feld <strong>Transfertyp</strong> des Abschnitts <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" aus. Die Standardeinstellung ist <strong>Importieren</strong>.  </p><p><strong>HINWEIS</strong>: Der <STRONG>Link</STRONG>-Transfertyp wird für Access-Projekte (ADP) nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tabellenkalkulationstyp</strong></p></td>
<td><p>Der Tabellenkalkulationstyp, in den importiert, aus dem exportiert oder zu dem eine Verknüpfung hergestellt werden soll. Sie können einen der im Feld aufgeführten Tabellenkalkulationstypen auswählen. Die Standardeinstellung ist <strong>Excel-Arbeitsmappe</strong>.  </p><p><strong>HINWEIS</strong>: Sie können Lotus. WK4-Dateien (schreibgeschützt) importieren und verknüpfen, aber Sie können keine Access-Daten in dieses Tabellenkalkulationsformat exportieren. Access unterstützt auch nicht mehr den Import, den Export oder das Verknüpfen von Daten aus Lotus. WKS- oder Excel-Version 2.0-Tabellen mit dieser Aktion. Wenn Sie Tabellenkalkulationsdaten im Format Excel, Version 2.0 oder Lotus .WKS importieren oder verknüpfen möchten, konvertieren Sie die Daten in eine neuere Version von Excel oder Lotus 1-2-3, bevor Sie sie in Access importieren oder mit Access verknüpfen.</p>
</td>
</tr>
<tr class="odd">
<td><p><strong>Tabellenname</strong></p></td>
<td><p>Der Name der Access-Tabelle, in die Tabellenkalkulationsdaten importiert, aus der solche Daten exportiert bzw. mit der solche Daten verknüpft werden sollen. Sie können auch den Namen der Access-Auswahlabfrage eingeben, aus der Sie Daten exportieren möchten. Dies ist ein erforderliches Argument. Wenn Sie <strong>Importieren</strong> im Argument <strong>Transfertyp</strong> auswählen, hängt Access die Tabellenkalkulationsdaten an diese Tabelle an, sofern die Tabelle bereits vorhanden ist. Andernfalls erstellt Access eine neue Tabelle mit den Tabellenkalkulationsdaten. In Access können Sie bei Verwendung der <strong>ImportExportSpreadsheet</strong> -Aktion keine SQL-Anweisung verwenden, um die zu exportierenden Daten anzugeben. Anstatt eine SQL-Anweisung zu verwenden, müssen Sie zunächst eine Abfrage erstellen und dann den Namen der Abfrage im Argument <strong>Tabellenname</strong> angeben.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Dateiname</strong></p></td>
<td><p>Der Name der Tabellenkalkulationsdatei, aus der importiert, in die exportiert bzw. mit der verknüpft werden soll. Geben Sie den vollständigen Pfad an. Dies ist ein erforderliches Argument. Wenn Sie Daten aus Access exportieren, erstellt Access eine neue Tabellenkalkulation. Wenn der Dateiname mit dem Namen einer vorhandenen Tabellenkalkulation identisch ist, ersetzt Access die vorhandene Tabellenkalkulation, es sei denn, Sie exportieren in eine Excel-Arbeitsmappe der Version 5.0 oder höher. In diesem Fall kopiert Access die exportierten Daten in das nächste verfügbare neue Arbeitsblatt in der Arbeitsmappe. Beim Importieren aus oder Verknüpfen mit einer Excel-Tabellenkalkulation der Version 5.0 oder höher können Sie das Argument <strong>Bereich</strong> verwenden, um ein bestimmtes Arbeitsblatt anzugeben.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Besitzt Feldnamen</strong></p></td>
<td><p>Gibt an, ob die erste Zeile der Tabellenkalkulation die Namen der Felder enthält. Wenn Sie <strong>Ja</strong> wählen, verwendet Access die Namen in dieser Zeile beim Importieren oder Verknüpfen der Tabellenkalkulationsdaten als Feldnamen in der Access-Tabelle. Wenn Sie <strong>Nein</strong> wählen, behandelt Access die erste Zeile als normale Zeile mit Daten. Die Standardeinstellung ist <strong>Nein</strong>. Wenn Sie eine Access-Tabelle oder -Auswahlabfrage in eine Tabellenkalkulation exportieren, werden die Feldnamen in die erste Zeile der Tabellenkalkulation eingefügt, unabhängig davon, was Sie in diesem Argument auswählen.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Range</strong></p></td>
<td><p>Der Bereich von Zellen, der importiert oder verknüpft werden soll. Lassen Sie dieses Argument leer, um die gesamten Tabellenkalkulation zu importieren oder zu verknüpfen. Sie können den Namen eines Bereichs in der Tabellenkalkulation eingeben oder den zu importierenden oder zu verknüpfenden Zellenbereich angeben, z. B. A1:E25 (beachten Sie, dass die A1..E25-Syntax in Access 97 oder höher nicht funktioniert). Wenn Sie aus einer Excel-Tabellenkalkulation der Version 5.0 oder höher importieren bzw. mit dieser verknüpfen, können Sie dem Bereich den Namen des Arbeitsblatts und ein Ausrufezeichen voranstellen; z. B. Budget!A1:C7.</p><p><strong>HINWEIS</strong>: Wenn Sie in eine Kalkulationstabelle exportieren, müssen Sie dieses Argument leer lassen. Wenn Sie einen Bereich eingeben, schlägt der Exportvorgang fehl.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die Daten in Access-Auswahlabfragen in Tabellenkalkulationen exportieren. Access exportiert das Resultset der Abfrage und behandelt es wie eine Tabelle.

Tabellenkalkulationsdaten, die Sie an eine vorhandene Access-Tabelle anfügen, müssen mit der Struktur der Tabelle kompatibel sein.

- Jedes Feld in der Tabellenkalkulation muss den gleichen Datentyp haben wie das entsprechende Feld in der Tabelle.

- Die Felder müssen in derselben Reihenfolge vorliegen (es sei denn, Sie legen das Argument **Besitzt Feldnamen** auf **Ja** fest; in diesem Fall müssen die Feldnamen in der Tabellenkalkulation mit den Feldnamen in der Tabelle übereinstimmen).

Diese Aktion entspricht dem Klicken auf die Registerkarte **Externe Daten** und dem Klicken auf **Excel** in der Gruppe **Importieren** oder **Exportieren** oder dem Klicken auf **Mehr** in der Gruppe **Importieren** oder **Exportieren** und dem Klicken auf **Lotus-1-2-3-Datei**. Sie können diese Befehle verwenden, um eine Datenquelle wie z. B. Access oder einen Datenbank-, Tabellenkalkulations- oder Textdateityp auszuwählen. Wenn Sie eine Tabellenkalkulation auswählen, wird eine Reihe von Dialogfeldern angezeigt oder ein Access-Assistent ausgeführt, in dem Sie den Namen der Tabellenkalkulation und andere Optionen auswählen. Die Argumente der **ImportExportSpreadsheet** -Aktion entsprechen den Optionen in diesen Dialogfeldern oder in den Assistenten.

> [!NOTE]
> Beim Abfragen oder Filtern einer verknüpften Tabellenkalkulation wird die Groß-/Kleinschreibung beachtet.

Wenn Sie eine Verknüpfung mit einer Excel-Tabellenkalkulation herstellen, die im Bearbeitungsmodus geöffnet ist, stellt Access die Verknüpfung erst dann her, wenn die Excel-Tabellenkalkulation den Bearbeitungsmodus verlassen hat. Es gibt kein Timeout.

Zum Ausführen der **ImportExportSpreadsheet** -Aktion in einem Visual Basic for Applications (VBA)-Modul verwenden Sie die **TransferSpreadsheet** -Methode des **DoCmd** -Objekts.

