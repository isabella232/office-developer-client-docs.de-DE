---
title: ImportExportText-Makroaktion
TOCTitle: ImportExportText macro action
ms:assetid: 366fa095-6f09-7c22-e734-bfa585cfe79e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192475(v=office.15)
ms:contentKeyID: 48544171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168097
f1_categories:
- Office.Version=v15
ms.openlocfilehash: be5497b7f1dbed4d32f25f2a675c3f996ed47c9f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925450"
---
# <a name="importexporttext-macro-action"></a>ImportExportText-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können die **Importierenexportierentext** -Aktion verwenden, um Text zwischen der aktuellen Microsoft Access-Datenbank (MDB oder ACCDB) oder Access-Projekt (ADP) und einer Textdatei importieren oder exportieren. Sie können auch die Daten in eine Textdatei mit der aktuellen Access-Datenbank verknüpfen. Mit einer verknüpften Textdatei können Sie die Textdaten mit Access anzeigen, wobei weiterhin uneingeschränkten Zugriff auf die Daten aus dem Programm Textverarbeitung. Sie können auch importieren aus zu exportieren und link zu einer Tabelle oder Liste in einer HTML-Datei (\*.html).

> [!NOTE]
> [!HINWEIS] Wenn Sie eine Verknüpfung mit Daten in einer Textdatei oder HTML-Datei herstellen, sind die Daten in Access schreibgeschützt.
> 
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ImportExportText** -Aktion hat die folgenden Argumente.

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
<td><p>Der Transfertyp, den Sie vornehmen möchten. Sie können Daten aus Textdateien mit Trennzeichen oder festgelegtem Format oder aus HTML-Dateien importieren, in sie exportieren oder eine Verknüpfung mit Daten in diesen Dateien herstellen. Außerdem können Sie Daten in eine Microsoft Word-Seriendruck-Datendatei exportieren, anhand der Sie anschließend mit dem Word-Seriendruckfeature Seriendruckdokumente wie z. B. Serienbriefe und Adressetiketten erstellen können. Wählen Sie <strong>Import mit Trennzeichen</strong>, <strong>Import festgelegtes Format</strong>, <strong>Import HTML</strong>, <strong>Export mit Trennzeichen</strong>, <strong>Export festgelegtes Format</strong>, <strong>Export HTML</strong>, <strong>Export Word für Windows-Seriendruck</strong>, <strong>Verknüpfung mit Trennzeichen</strong> <strong>Verknüpfung festgelegtes Format</strong> oder <strong>Verknüpfung HTML</strong> im Feld <strong>Transfertyp</strong> des Abschnitts <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" aus. Die Standardeinstellung ist <strong>Import mit Trennzeichen</strong>.  </p>

> [!NOTE]
> <P>In einem Access-Projekt (.adp) werden nur <STRONG>Import mit Trennzeichen</STRONG>, <STRONG>Import festgelegtes Format</STRONG>, <STRONG>Export mit Trennzeichen</STRONG>, <STRONG>Export festgelegtes Format</STRONG> oder <STRONG>Export Word für Windows-Seriendruck</STRONG> unterstützt.</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Spezifikationsname</strong></p></td>
<td><p>Der Spezifikationsname für den Satz von Optionen, der bestimmt, wie eine Textdatei importiert oder verknüpft wird. Für eine Textdatei mit festgelegtem Format müssen Sie entweder ein Argument angeben oder eine schema.ini-Datei verwenden, die in demselben Ordner wie die importierte oder verknüpfte Textdatei gespeichert sein muss.  </p>
<p>So erstellen Sie eine Spezifikation zum Importieren oder Verknüpfen einer Textdatei</p>
<ol>
<li><p>Geben Sie im Dialogfeld <strong>Externe Daten</strong> den Pfad der Quelltextdatei in das Feld <strong>Dateiname</strong> ein.</p></li>
<li><p>Klicken Sie auf die gewünschte Option zum Speichern der Daten (Importieren, Anfügen oder Verknüpfen), und klicken Sie auf <strong>OK</strong>.</p></li>
<li><p>Klicken Sie im Dialogfeld <strong>Textimport-Assistent</strong> auf <strong>Erweitert</strong>.</p></li>
<li><p>Geben Sie die gewünschten Optionen für diese Spezifikation an, und klicken Sie auf <strong>Speichern unter</strong>.</p></li>
<li><p>Geben Sie den gewünschten Namen für die Spezifikation ein, und klicken Sie dann auf <strong>OK</strong>.</p></li>
<li><p>Sie können vorhandene Spezifikationen verwalten, indem Sie im Spezifikationsdialogfeld auf <strong>Spezifikationen</strong> klicken.</p></li>
<li><p>Klicken Sie auf <strong>OK</strong>, um das Spezifikationsdialogfeld zu schließen.</p></li>
</ol>
<p></p>
<p>Anschließend können Sie den Spezifikationsnamen immer dann in dieses Argument eingeben, wenn Sie eine Textdatei des gleichen Typs importieren oder exportieren möchten. Sie können Textdateien mit Trennzeichen importieren, exportieren oder verknüpfen, ohne einen Spezifikationsnamen für dieses Argument einzugeben. In diesem Fall verwendet Access die Standardeinstellungen aus dem Dialogfeld des Assistenten. Access verwendet ein vordefiniertes Format für Seriendruck-Datendateien, sodass Sie nie einen Spezifikationsnamen für dieses Argument eingeben müssen, wenn Sie diese Dateitypen exportieren. Sie können Import-/Exportspezifikationen mit HTML-Dateien verwenden, allerdings ist dann als einziger Teil der Spezifikation die Spezifikation für die Datentypformatierung anwendbar.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Tabellenname</strong></p></td>
<td><p>Der Name der Access-Tabelle, in die Textdaten importiert, aus der Textdaten exportiert bzw. mit der Textdaten verknüpft werden sollen. Sie können auch den Namen der Access-Abfrage eingeben, aus der Sie Daten exportieren möchten. Dies ist ein erforderliches Argument. Wenn Sie im Feld <strong>Transfertyp</strong> auf <strong>Import mit Trennzeichen</strong>, <strong>Import festgelegtes Format</strong> oder <strong>Import HTML</strong> klicken, fügt Access die Textdaten an diese Tabelle an, sofern die Tabelle bereits vorhanden ist. Andernfalls erstellt Access eine neue Tabelle mit den Textdaten. Bei Verwendung der <strong>ImportExportText</strong> -Aktion können Sie keine SQL-Anweisung verwenden, um die zu exportierenden Daten anzugeben. Anstatt eine SQL-Anweisung zu verwenden, müssen Sie zunächst eine Abfrage erstellen und dann den Namen der Abfrage im Argument <strong>Tabellenname</strong> angeben.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Dateiname</strong></p></td>
<td><p>Der Name der Textdatei, aus der importiert, in die exportiert bzw. mit der verknüpft werden soll. Geben Sie den vollständigen Pfad an. Dies ist ein erforderliches Argument. Wenn Sie Daten aus Access exportieren, erstellt Access eine neue Textdatei. Wenn der Dateiname mit dem Namen einer vorhandenen Textdatei identisch ist, ersetzt Access die vorhandene Textdatei. Wenn Sie eine bestimmte Tabelle oder Liste in einer HTML-Datei importieren oder verknüpfen möchten, können Sie das Argument <strong>HTML-Tabellenname</strong> verwenden.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Besitzt Feldnamen</strong></p></td>
<td><p>Gibt an, ob die erste Zeile der Textdatei die Namen der Felder enthält. Wenn Sie <strong>Ja</strong> wählen, verwendet Access die Namen in dieser Zeile beim Importieren oder Verknüpfen der Textdaten als Feldnamen in der Access-Tabelle. Wenn Sie <strong>Nein</strong> wählen, behandelt Access die erste Zeile als normale Zeile mit Daten. Die Standardeinstellung ist <strong>Nein</strong>. Access ignoriert dieses Argument für Word für Windows-Seriendruck-Datendateien, da die erste Zeile die Feldnamen enthalten muss. Wenn Sie eine Access-Tabelle oder -Auswahlabfrage in eine Textdatei mit Trennzeichen oder festgelegtem Format exportieren, fügt Access die Feldnamen der Tabelle oder Auswahlabfrage in die erste Zeile der Textdatei ein, sofern Sie <strong>Ja</strong> für dieses Argument ausgewählt haben. Wenn Sie eine Textdatei mit festgelegtem Format importieren oder verknüpfen und in diesem Feld <strong>Ja</strong> auswählen, muss in der ersten Zeile mit den Feldnamen das Feldtrennzeichen verwendet werden, das in der Import-/Exportspezifikation zum Trennen der Feldnamen festgelegt wurde. Wenn Sie in eine Textdatei mit festgelegtem Format exportieren und <strong>Ja</strong> für dieses Argument auswählen, fügt Access die Feldnamen mit diesem Trennzeichen in die erste Zeile der Textdatei ein.  </p></td>
</tr>
<tr class="even">
<td><p><strong>HTML-Tabellenname</strong></p></td>
<td><p>Der Name der Tabelle oder Liste in der HTML-Datei, die Sie importieren oder verknüpfen möchten. Dieses Argument wird ignoriert, es sei denn, das Argument <strong>Transfertyp</strong> auf Import HTML oder Verknüpfung HTML festgelegt ist. Wenn Sie dieses Argument leer lassen, wird die erste Tabelle oder Liste in der HTML-Datei importiert oder verknüpft. Name der Tabelle oder Liste in der HTML-Datei wird durch den angegebenen Text bestimmt die &lt;Beschriftung&gt; markieren, wenn es ist eine &lt;Beschriftung&gt; Tag. Wenn kein &lt;CAPTION&gt; -Tag vorhanden ist, wird der Name durch den vom &lt;TITLE&gt;-Tag angegebenen Text bestimmt. Wenn mehr als eine Tabelle oder Liste, den denselben Namen hat, werden Sie von Access durch Hinzufügen einer Zahl am Ende der einzelnen Namen unterscheidet; Personal1 und Mitarbeiter2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Codepage</strong></p></td>
<td><p>Der Name des Zeichensatzes, der mit der Codepage verwendet wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die Daten in Access-Auswahlabfragen in Textdateien exportieren. Access exportiert das Resultset der Abfrage und verarbeitet es wie eine Tabelle.

Textdaten, die Sie an eine vorhandene Access-Tabelle anfügen, müssen mit der Struktur der Tabelle kompatibel sein.

- Jedes Feld im Text muss den gleichen Datentyp aufweisen wie das entsprechende Feld in der Tabelle.

- Die Felder müssen in derselben Reihenfolge vorliegen (es sei denn, Sie legen das Argument **Besitzt Feldnamen** auf **Ja** fest; in diesem Fall müssen die Feldnamen im Text mit den Feldnamen in der Tabelle übereinstimmen).

Diese Aktion entspricht dem Klicken auf **Textdatei** in der Gruppe **Importieren** oder **Exportieren** der Registerkarte **Externe Daten**. Die Argumente der **ImportExportText** -Aktion entsprechen den Optionen des Assistenten, der mit dem Befehl **Textdatei** gestartet wird.

> [!TIP]
> [!TIPP] Eine Import-/Exportspezifikation speichert die Informationen, die Access zum Importieren, Exportieren oder Verknüpfen einer Textdatei benötigt. Sie können gespeicherte Spezifikationen zum Importieren, Exportieren oder Verknüpfen von Textdaten in, aus bzw. mit ähnlichen Textdateien verwenden. Beispiel: Sie erhalten wöchentliche Umsatzzahlen in einer Textdatei von einem Mainframecomputer. Sie können eine Spezifikation für diese Art von Daten erstellen und speichern und die Spezifikation immer dann verwenden, wenn Sie diese Daten zu Ihrer Access-Datenbank hinzufügen.

> [!NOTE]
> [!HINWEIS] Beim Abfragen oder Filtern einer verknüpften Textdatei wird die Groß-/Kleinschreibung beachtet.

Zum Ausführen der **ImportExportText** -Aktion in einem Visual Basic for Applications (VBA)-Modul verwenden Sie die **TransferText** -Methode des **DoCmd** -Objekts.

