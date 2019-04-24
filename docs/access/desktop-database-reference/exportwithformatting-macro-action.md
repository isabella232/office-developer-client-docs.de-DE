---
title: ExportWithFormatting-Makroaktion
TOCTitle: ExportWithFormatting macro action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb633977fcc1b39fc2a5c0bb69523bc93c193695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293210"
---
# <a name="exportwithformatting-macro-action"></a>ExportWithFormatting-Makroaktion


**Gilt für**: Access 2013, Office 2013

Mit der **ExportierenMitFormatierung**-Aktion können Sie Daten aus einem bestimmten Microsoft Access-Datenbankobjekt (Datenblatt, Formular, Bericht, Modul, Datenzugriffsseite) in verschiedene Formate ausgeben.

## <a name="settings"></a>Einstellungen

Die **ExportierenMitFormatierung**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Objekttyp</strong></p></td>
<td><p>Der Typ des Objekts, das die auszugebenden Daten enthält. Klicken Sie im Fenster <strong>Objekttyp</strong> im Bereich <strong>Aktionsargumente</strong> der Leiste "Makro-Generator" auf <strong>Tabelle</strong> (für ein Tabellendatenblatt), <strong>Abfrage</strong> (für ein Abfragedatenblatt), <strong>Formular</strong> (für ein Formular oder Formulardatenblatt), <strong>Bericht</strong>, <strong>Modul</strong>, <strong>Serveransicht</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Sie können kein Makro ausgeben. Wenn Sie das aktive Objekt ausgeben möchten, wählen Sie den passenden Objekttyp mit diesem Argument aus, aber lassen Sie das <strong>Objektname</strong>-Argument leer. Dabei handelt es sich um ein Pflichtargument. Der Standardwert ist <strong>Tabelle</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des Objekts, das die auszugebenden Daten enthält. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank mit dem Objekttyp angezeigt, der mit dem <strong>Objekttyp</strong> -Argument ausgewählt wurde. Wenn Sie ein Makro mit der <strong>ExportierenMitFormatierung</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Access zuerst in der Bibliotheksdatenbank nach dem Objekt mit diesem Namen und erst dann in der geöffneten Datenbank.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Ausgabeformat</strong></p></td>
<td><p>Das Dateiformat, das Sie für die Ausgabe der Daten verwenden möchten. Dabei stehen die Dateiformate <strong>Excel 97 - Excel 2003-Arbeitsmappe (*.xls)</strong>, <strong>Excel-Binärarbeitsmappe (*.xlsb)</strong>, <strong>Excel-Arbeitsmappe (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95-Arbeitsmappe (*.xls)</strong>, <strong>PDF-Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Textdatei (*.txt)</strong> und <strong>XPS-Format (*.xps)</strong> zur Auswahl. Wenn Sie dieses Argument leer lassen, werden Sie von Access zur Angabe eines Dateiformats aufgefordert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ausgabedatei</strong></p></td>
<td><p>Die Datei, in die die Daten ausgegeben werden sollen, einschließlich des vollständigen Dateipfads. Sie können die standardmäßige Dateierweiterung für das Ausgabeformat angeben, das Sie mit dem Argument <strong>Ausgabeformat</strong> ausgewählt haben, dies ist jedoch nicht erforderlich. Wenn Sie das Argument <strong>Ausgabedatei</strong> leer lassen, werden Sie von Access aufgefordert, einen Namen für die Ausgabedatei anzugeben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Autostart</strong></p></td>
<td><p>Hiermit können Sie festlegen, ob direkt nach der Ausführung einer <strong>ExportierenMitFormatierung</strong>-Aktion ein entsprechendes Programm für die im Argument <strong>Ausgabedatei</strong> festgelegte Datei geöffnet werden soll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Vorlagendatei</strong></p></td>
<td><p>Der Pfad und Dateiname einer Datei, die Sie als Vorlage für HTML-Dateien verwenden möchten. Die Vorlagendatei ist eine Textdatei, die für Access eindeutige HTML-Tags und Token enthält.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Codierung</strong></p></td>
<td><p>Die Zeichencodierung, mit der Sie den Text oder die HTML-Daten ausgeben möchten. Dabei stehen die Codierungen <strong>MS-DOS</strong>, <strong>Unicode</strong> und <strong>Unicode (UTF-8)</strong> zur Auswahl. Das Argument <strong>MS-DOS</strong> ist nur für Textdateien verfügbar. Wenn Sie dieses Argument leer lassen, verwendet Access die Windows-Standardcodierung für Textdateien und die standardmäßige Systemcodierung für HTML-Dateien.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ausgabequalität</strong></p></td>
<td><p>Wählen Sie <strong>Drucken</strong> aus, um die Ausgabe für den Druck zu optimieren, oder <strong>Bildschirm</strong>, um die Ausgabe für die Bildschirmanzeige zu optimieren.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die Access-Daten werden im ausgewählten Format ausgegeben und können von jeder Anwendung gelesen werden, die das gleiche Format verwendet. Sie können einen Access-Bericht beispielsweise mit seiner Formatierung in ein RTF-Dokument ausgeben und das Dokument anschließend in Microsoft Word öffnen.

Wenn Sie das Datenbankobjekt in HTML-Format ausgeben, erstellt Access eine Datei im HTML-Format mit den Daten aus dem Objekt. Sie können mit dem Argument **Vorlagendatei** eine Datei angeben, die als Vorlage für die HTML-Datei verwendet werden soll.

Für alle Ausgabeformate gelten die folgenden Regeln, wenn Sie ein Datenbankobjekt mit der Aktion **ExportierenMitFormatierung** ausgeben:

  - Sie können Daten in eine Tabelle, Abfragen und Formulardatenblättern ausgeben. In der Ausgabedatei werden alle Felder so angezeigt, wie in Access. Ausgenommen hiervon sind OLE-Objekte. Die Spalten für die Felder eines OLE-Objekts werden zwar ausgegeben, sind aber leer.

  - Für ein Steuerelement, das an ein Ja/Nein-Feld gebunden ist (Umschaltfläche, Optionsschaltfläche oder Kontrollkästchen) wird in der Ausgabedatei der Wert "-1 (Ja)" oder "0 (Nein)" angezeigt.

  - Für ein Textfeld, das an ein Hyperlink-Feld gebunden ist wird in der Ausgabedatei der Hyperlink angezeigt. Davon ausgenommen sind MS-DOS-Textdateien, bei denen der Hyperlink als reiner Text angezeigt wird.

  - Wenn Sie die Daten aus einem Formular in der Formularansicht ausgeben, enthält die Ausgabedatei immer die Datenblattansicht.

  - Wenn Sie ein Datenblatt, Formular oder eine Datenzugriffsseite im HTML-Format ausgeben, wird eine HTML-Datei erstellt. Wenn Sie einen Bericht im HTML-Format ausgeben, wird für jede Seite im Bericht eine HTML-Datei erstellt.

Das Ergebnis der Ausführung der **ExportierenMitFormatierung**-Aktion entspricht dem Klicken auf eine der Optionen in der Gruppe **Export** auf der Registerkarte **Externe Daten**. Die Aktionsargumente entsprechen den Einstellungen im Dialogfeld **Export**.

Zum Ausführen der **ExportierenMitFormatierung**-Aktion in einem Visual Basic for Applications (VBA)-Modul verwenden Sie die **OutputTo**-Methode des **DoCmd**-Objekts.

