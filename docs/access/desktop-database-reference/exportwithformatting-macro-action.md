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
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="aacbc-102">ExportWithFormatting-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="aacbc-102">ExportWithFormatting macro action</span></span>


<span data-ttu-id="aacbc-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aacbc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aacbc-104">Mit der **ExportierenMitFormatierung**-Aktion können Sie Daten aus einem bestimmten Microsoft Access-Datenbankobjekt (Datenblatt, Formular, Bericht, Modul, Datenzugriffsseite) in verschiedene Formate ausgeben.</span><span class="sxs-lookup"><span data-stu-id="aacbc-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="aacbc-105">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="aacbc-105">Settings</span></span>

<span data-ttu-id="aacbc-106">Die **ExportierenMitFormatierung**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="aacbc-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aacbc-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="aacbc-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="aacbc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aacbc-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aacbc-109"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-p101">Der Typ des Objekts, das die auszugebenden Daten enthält. Klicken Sie im Fenster <strong>Objekttyp</strong> im Bereich <strong>Aktionsargumente</strong> der Leiste "Makro-Generator" auf <strong>Tabelle</strong> (für ein Tabellendatenblatt), <strong>Abfrage</strong> (für ein Abfragedatenblatt), <strong>Formular</strong> (für ein Formular oder Formulardatenblatt), <strong>Bericht</strong>, <strong>Modul</strong>, <strong>Serveransicht</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Sie können kein Makro ausgeben. Wenn Sie das aktive Objekt ausgeben möchten, wählen Sie den passenden Objekttyp mit diesem Argument aus, aber lassen Sie das <strong>Objektname</strong>-Argument leer. Dabei handelt es sich um ein Pflichtargument. Der Standardwert ist <strong>Tabelle</strong>.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p101">The type of object containing the data to output. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't output a macro. If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank. This is a required argument. The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aacbc-116"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-p102">Der Name des Objekts, das die auszugebenden Daten enthält. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank mit dem Objekttyp angezeigt, der mit dem <strong>Objekttyp</strong> -Argument ausgewählt wurde. Wenn Sie ein Makro mit der <strong>ExportierenMitFormatierung</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Access zuerst in der Bibliotheksdatenbank nach dem Objekt mit diesem Namen und erst dann in der geöffneten Datenbank.  </span><span class="sxs-lookup"><span data-stu-id="aacbc-p102">The name of the object containing the data to output. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aacbc-120"><strong>Ausgabeformat</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-p103">Das Dateiformat, das Sie für die Ausgabe der Daten verwenden möchten. Dabei stehen die Dateiformate <strong>Excel 97 - Excel 2003-Arbeitsmappe (*.xls)</strong>, <strong>Excel-Binärarbeitsmappe (*.xlsb)</strong>, <strong>Excel-Arbeitsmappe (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95-Arbeitsmappe (*.xls)</strong>, <strong>PDF-Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Textdatei (*.txt)</strong> und <strong>XPS-Format (*.xps)</strong> zur Auswahl. Wenn Sie dieses Argument leer lassen, werden Sie von Access zur Angabe eines Dateiformats aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p103">The type of format you want to use to output the data. You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>. If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aacbc-124"><strong>Ausgabedatei</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-p104">Die Datei, in die die Daten ausgegeben werden sollen, einschließlich des vollständigen Dateipfads. Sie können die standardmäßige Dateierweiterung für das Ausgabeformat angeben, das Sie mit dem Argument <strong>Ausgabeformat</strong> ausgewählt haben, dies ist jedoch nicht erforderlich. Wenn Sie das Argument <strong>Ausgabedatei</strong> leer lassen, werden Sie von Access aufgefordert, einen Namen für die Ausgabedatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p104">The file to which you want to output the data, including the full path. You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required. If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aacbc-128"><strong>Autostart</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-129">Hiermit können Sie festlegen, ob direkt nach der Ausführung einer <strong>ExportierenMitFormatierung</strong>-Aktion ein entsprechendes Programm für die im Argument <strong>Ausgabedatei</strong> festgelegte Datei geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aacbc-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aacbc-130"><strong>Vorlagendatei</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-p105">Der Pfad und Dateiname einer Datei, die Sie als Vorlage für HTML-Dateien verwenden möchten. Die Vorlagendatei ist eine Textdatei, die für Access eindeutige HTML-Tags und Token enthält.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p105">The path and file name of a file you want to use as a template for HTML files. The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aacbc-133"><strong>Codierung</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-p106">Die Zeichencodierung, mit der Sie den Text oder die HTML-Daten ausgeben möchten. Dabei stehen die Codierungen <strong>MS-DOS</strong>, <strong>Unicode</strong> und <strong>Unicode (UTF-8)</strong> zur Auswahl. Das Argument <strong>MS-DOS</strong> ist nur für Textdateien verfügbar. Wenn Sie dieses Argument leer lassen, verwendet Access die Windows-Standardcodierung für Textdateien und die standardmäßige Systemcodierung für HTML-Dateien.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p106">The type of character encoding format you want used to output the text or HTML data. You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>. The <strong>MS-DOS</strong> argument setting is available only for text files. If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aacbc-138"><strong>Ausgabequalität</strong></span><span class="sxs-lookup"><span data-stu-id="aacbc-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="aacbc-139">Wählen Sie <strong>Drucken</strong> aus, um die Ausgabe für den Druck zu optimieren, oder <strong>Bildschirm</strong>, um die Ausgabe für die Bildschirmanzeige zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="aacbc-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aacbc-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aacbc-140">Remarks</span></span>

<span data-ttu-id="aacbc-p107">Die Access-Daten werden im ausgewählten Format ausgegeben und können von jeder Anwendung gelesen werden, die das gleiche Format verwendet. Sie können einen Access-Bericht beispielsweise mit seiner Formatierung in ein RTF-Dokument ausgeben und das Dokument anschließend in Microsoft Word öffnen.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p107">The Access data is output in the selected format and can be read by any program that uses the same format. For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="aacbc-p108">Wenn Sie das Datenbankobjekt in HTML-Format ausgeben, erstellt Access eine Datei im HTML-Format mit den Daten aus dem Objekt. Sie können mit dem Argument **Vorlagendatei** eine Datei angeben, die als Vorlage für die HTML-Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p108">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object. You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="aacbc-145">Für alle Ausgabeformate gelten die folgenden Regeln, wenn Sie ein Datenbankobjekt mit der Aktion **ExportierenMitFormatierung** ausgeben:</span><span class="sxs-lookup"><span data-stu-id="aacbc-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="aacbc-p109">Sie können Daten in eine Tabelle, Abfragen und Formulardatenblättern ausgeben. In der Ausgabedatei werden alle Felder so angezeigt, wie in Access. Ausgenommen hiervon sind OLE-Objekte. Die Spalten für die Felder eines OLE-Objekts werden zwar ausgegeben, sind aber leer.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p109">You can output data in table, query, and form datasheets. In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects. The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="aacbc-149">Für ein Steuerelement, das an ein Ja/Nein-Feld gebunden ist (Umschaltfläche, Optionsschaltfläche oder Kontrollkästchen) wird in der Ausgabedatei der Wert "-1 (Ja)" oder "0 (Nein)" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aacbc-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value -1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="aacbc-150">Für ein Textfeld, das an ein Hyperlink-Feld gebunden ist wird in der Ausgabedatei der Hyperlink angezeigt. Davon ausgenommen sind MS-DOS-Textdateien, bei denen der Hyperlink als reiner Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aacbc-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="aacbc-151">Wenn Sie die Daten aus einem Formular in der Formularansicht ausgeben, enthält die Ausgabedatei immer die Datenblattansicht.</span><span class="sxs-lookup"><span data-stu-id="aacbc-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="aacbc-p110">Wenn Sie ein Datenblatt, Formular oder eine Datenzugriffsseite im HTML-Format ausgeben, wird eine HTML-Datei erstellt. Wenn Sie einen Bericht im HTML-Format ausgeben, wird für jede Seite im Bericht eine HTML-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="aacbc-p110">When you output a datasheet, form, or data access page in HTML format, one .html file is created. When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="aacbc-154">Das Ergebnis der Ausführung der **ExportierenMitFormatierung**-Aktion entspricht dem Klicken auf eine der Optionen in der Gruppe **Export** auf der Registerkarte **Externe Daten**. Die Aktionsargumente entsprechen den Einstellungen im Dialogfeld **Export**.</span><span class="sxs-lookup"><span data-stu-id="aacbc-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="aacbc-155">Zum Ausführen der **ExportierenMitFormatierung**-Aktion in einem Visual Basic for Applications (VBA)-Modul verwenden Sie die **OutputTo**-Methode des **DoCmd**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aacbc-155">To run the **ExportWithFormatting** action in a Visual Basic for Applications (VBA) module, use the **OutputTo** method of the **DoCmd** object.</span></span>

