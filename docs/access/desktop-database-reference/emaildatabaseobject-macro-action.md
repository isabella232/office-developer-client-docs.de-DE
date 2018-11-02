---
title: EMailDatenbankobjekt-Makroaktion
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f0c0ba73274d6f27a9e2a857aea1061416168f3a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922916"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="88012-102">EMailDatenbankobjekt-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="88012-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="88012-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="88012-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="88012-104">Verwenden Sie die **EMailDatenbankobjekt** -Aktion, um ein angegebenes Datenblatt, ein Formular, einen Bericht, ein Modul oder eine Datenzugriffsseite von Microsoft Access zum Anzeigen oder Weiterleiten in eine E-Mail-Nachricht einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="88012-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="88012-p101">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="88012-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="settings"></a><span data-ttu-id="88012-107">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="88012-107">Settings</span></span>

<span data-ttu-id="88012-108">Die **EMailDatenbankobjekt** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="88012-108">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88012-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="88012-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="88012-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88012-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88012-111"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="88012-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p102">Der in die E-Mail-Nachricht einzuschließende Objekttyp. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle (für ein Tabellendatenblatt), auf Abfrage (für ein Abfragedatenblatt), auf Formular (für ein Formular oder Formulardatenblatt), auf Bericht, auf Modul oder auf Datenzugriffsseite, auf Serversicht, auf Gespeicherte Prozedur oder auf Funktion. Sie können kein Makro senden. Wenn Sie das aktive Objekt einschließen möchten, wählen Sie dessen Typ mit diesem Argument aus, lassen Sie jedoch das Argument Objektname leer.</span><span class="sxs-lookup"><span data-stu-id="88012-p102">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88012-116"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="88012-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p103">Der Name des Objekts, das zu der E-Mail hinzugefügt werden soll. Das Feld <strong>Objektname</strong> zeigt alle Objekte in der Datenbank vom Typ, der im <strong>Objekttyp</strong> -Argument ausgewählt ist. Wenn Sie die Argumente <strong>Objekttyp</strong> und <strong>Objektname</strong> leer lassen, sendet Access eine Nachricht an die E-Mail-Anwendung ohne ein Datenbankobjekt. Wenn Sie ein Makro mit der <strong>EMailDatenbankobjekt</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Access nach dem Objekt mit diesem Namen zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank.  </span><span class="sxs-lookup"><span data-stu-id="88012-p103">The name of the object to include in the mail message. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object. If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88012-121"><strong>Ausgabeformat</strong></span><span class="sxs-lookup"><span data-stu-id="88012-121"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-122">Der Typ des Formats soll für das eingeschlossene Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="88012-122">The type of format you want used for the included object.</span></span> <span data-ttu-id="88012-123">Je nachdem, was Sie für das Argument <strong>Objekttyp</strong> auswählen ändert sich die Liste der Formate, die, denen Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="88012-123">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="88012-124"><strong>Excel 97 - 2003-Arbeitsmappe (*.xls)</strong>, <strong>Excel-Binärarbeitsmappe (.xlsb)</strong>, <strong>Excel-Arbeitsmappe (*.xlsx)</strong>verfügbaren Formate gehören <strong>HTML (*.htm, \* .html)</strong>, <strong>Microsoft Excel 5.0/95-Arbeitsmappe (*.xls)</strong>, <strong>PDF-Format </strong>, <strong>Dialog: Rich Text Format (*.RTF)</strong>, <strong>Textdateien (*.txt)</strong>oder <strong>XPS-Format (\*.XPS)</strong>.</span><span class="sxs-lookup"><span data-stu-id="88012-124">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="88012-125">im Feld <strong>Ausgabeformat</strong> .</span><span class="sxs-lookup"><span data-stu-id="88012-125">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="88012-126">Module können nur im Textformat gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="88012-126">Modules can be sent only in text format.</span></span> <span data-ttu-id="88012-127">Datenzugriffsseiten können nur im HTML-Format gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="88012-127">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="88012-128">Wenn Sie dieses Argument leer lassen, werden Sie von Access zur Angabe eines Dateiformats aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="88012-128">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88012-129"><strong>An</strong></span><span class="sxs-lookup"><span data-stu-id="88012-129"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p105">Die Empfänger der Nachricht, deren Namen in das Feld <strong>An</strong> der E-Mail-Nachricht aufgenommen werden sollen. Wenn Sie dieses Argument leer lassen, werden Sie von Access aufgefordert, die Namen der Empfänger anzugeben. Die Empfängernamen in diesem Argument 8sowie in den Argumenten <strong>Cc</strong> und <strong>Bcc</strong>) müssen durch Semikolons (;) oder durch das Listentrennzeichen voneinander getrennt werden, das in der Microsoft Windows- <strong>Systemsteuerung</strong> im Dialogfeld <strong>Ländereinstellungen</strong> auf der Registerkarte <strong>Zahlen</strong> festgelegt ist. Wenn die Empfängernamen nicht von der E-Mail-Anwendung erkannt werden, wird die Nachricht nicht gesendet, und es tritt ein Fehler auf.  </span><span class="sxs-lookup"><span data-stu-id="88012-p105">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88012-134"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="88012-134"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-135">Die Empfänger der Nachricht, deren Namen Sie in der <strong>Cc</strong> aufnehmen möchten (&quot;Carbon Copy, Blindkopie&quot;) Zeile in der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="88012-135">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="88012-136">Wenn Sie dieses Argument leer lassen, bleibt die <strong>Cc</strong>-Zeile der E-Mail-Nachricht leer.</span><span class="sxs-lookup"><span data-stu-id="88012-136">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88012-137"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="88012-137"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-138">Die Empfänger der Nachricht, deren Namen Sie in der <strong>Bcc</strong> aufnehmen möchten (&quot;blind Carbon Copy, Blindkopie&quot;) Zeile in der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="88012-138">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="88012-139">Wenn Sie dieses Argument leer lassen, bleibt die <strong>Bcc</strong>-Zeile der E-Mail-Nachricht leer.</span><span class="sxs-lookup"><span data-stu-id="88012-139">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88012-140"><strong>Betreff</strong></span><span class="sxs-lookup"><span data-stu-id="88012-140"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p108">Der Betreff der Nachricht. Dieser Text wird in der <strong>Betreff</strong>-Zeile der E-Mail-Nachricht angezeigt. Wenn Sie dieses Argument leer lassen, bleibt die <strong>Betreff</strong>-Zeile der E-Mail-Nachricht leer.  </span><span class="sxs-lookup"><span data-stu-id="88012-p108">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88012-144"><strong>Nachrichtentext</strong></span><span class="sxs-lookup"><span data-stu-id="88012-144"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p109">Beliebiger Text, den Sie zusätzlich in das Datenbankobjekt einschließen möchten. Dieser Text wird im Hauptteil der E-Mail-Nachricht nach dem Objekt angezeigt. Wenn Sie dieses Argument leer lassen, wird kein zusätzlicher Text in die E-Mail-Nachricht eingeschlossen. Lassen Sie die Argumente <strong>Objekttyp</strong> und <strong>Objektname</strong> leer, können Sie mit diesem Argument eine E-Mail-Nachricht ohne Datenbankobjekt senden.  </span><span class="sxs-lookup"><span data-stu-id="88012-p109">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88012-149"><strong>Nachricht bearbeiten</strong></span><span class="sxs-lookup"><span data-stu-id="88012-149"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p110">Gibt an, ob die Nachricht vor dem Senden bearbeitet werden kann. Wenn Sie <strong>Ja</strong> auswählen, wird die E-Mail-Anwendung automatisch gestartet, und die Nachricht kann bearbeitet werden. Wenn Sie <strong>Nein</strong> auswählen, wird die Nachricht gesendet, ohne dass der Benutzer eine Möglichkeit zur Bearbeitung hat. Die Standardeinstellung ist <strong>Ja</strong>.  </span><span class="sxs-lookup"><span data-stu-id="88012-p110">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88012-154"><strong>Vorlagedatei</strong></span><span class="sxs-lookup"><span data-stu-id="88012-154"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="88012-p111">Der Pfad und Dateiname einer Datei, die Sie als Vorlage für eine HTML-Datei verwenden möchten. Eine Vorlagedatei enthält HTML-Tags.</span><span class="sxs-lookup"><span data-stu-id="88012-p111">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="88012-157">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88012-157">Remarks</span></span>

<span data-ttu-id="88012-p112">Das Objekt in der E-Mail-Nachricht ist das ausgewählte Ausgabeformat. Beim Doppelklicken auf das Objekt wird die entsprechende Software gestartet und das Objekt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="88012-p112">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="88012-160">Die folgenden Regeln gelten bei der Verwendung der **EMailDatenbankobjekt** -Aktion zum Einschließen eines Datenbankobjekts in eine E-Mail-Nachricht:</span><span class="sxs-lookup"><span data-stu-id="88012-160">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="88012-p113">Sie können Tabellen-, Abfrage- und Formulardatenblätter senden. Im verwendeten Objekt sehen alle Felder im Datenblatt so aus wie in Access, mit Ausnahme der Felder, die OLE-Objekte enthalten. Die Spalten für diese Felder sind im Objekt eingeschlossen, die Felder sind jedoch leer.</span><span class="sxs-lookup"><span data-stu-id="88012-p113">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="88012-164">Für ein Steuerelement, das an ein Ja/Nein-Feld (eine Umschaltfläche, eine Optionsschaltfläche oder ein Kontrollkästchen) gebunden ist, wird in der Ausgabedatei der Wert –1 (Ja) oder 0 (Nein) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88012-164">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="88012-165">Für ein Textfeld, das an ein Hyperlink-Feld gebunden ist, wird in der Ausgabedatei der Hyperlink für alle Ausgabeformate mit Ausnahme von MS-DOS-Text angezeigt (in diesem Fall wird der Hyperlink nur als normaler Text angezeigt).</span><span class="sxs-lookup"><span data-stu-id="88012-165">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="88012-166">Wenn Sie ein Formular in der Formularansicht senden, enthält das eingeschlossene Objekt immer die Datenblattansicht des Objekts.</span><span class="sxs-lookup"><span data-stu-id="88012-166">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="88012-p114">Wenn Sie einen Bericht senden, sind Textfelder und (in einigen Fällen) Bezeichnungsfelder die einzigen Steuerelemente, die in das Objekt eingeschlossen werden. Alle sonstigen Steuerelemente werden ignoriert. Auch Kopf- und Fußzeileninformationen werden ausgeschlossen. Die einzige Ausnahme besteht darin, dass beim Senden eines Berichts im Excel-Format ein Textfeld in einem Gruppenfuß, das einen Ausdruck mit der **Summe** -Funktion enthält, in das Objekt eingeschlossen wird. Keine anderen Steuerelemente in einer Kopf- oder Fußzeile (und keine andere Aggregatfunktion als **Summe**) werden in das Objekt eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="88012-p114">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="88012-172">Unterberichte sind im Objekt eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="88012-172">Subreports are included in the object.</span></span>

- <span data-ttu-id="88012-p115">Wenn Sie ein Datenblatt, ein Formular oder eine Datenzugriffsseite im HTML-Format senden, wird eine HTML-Datei erstellt. Wenn Sie einen Bericht im HTML-Format senden, wird für jede Seite im Bericht eine HTML-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="88012-p115">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="88012-175">Verwenden Sie die **SendObject** -Methode des **DoCmd** -Objekts, um die **EMailDatenbankobjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="88012-175">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="88012-176">Über den Autor</span><span class="sxs-lookup"><span data-stu-id="88012-176">About the contributor</span></span>

<span data-ttu-id="88012-177">**Verknüpfung von bereitgestellt.** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), Gründer und Präsident von FMS, Inc., dem führenden Anbieter von kundendatenbanklösungen und Entwickler-Tools.</span><span class="sxs-lookup"><span data-stu-id="88012-177">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

  - [<span data-ttu-id="88012-178">Merkmale und Begrenzungen in Bezug auf die Verwendung der Methode „SendObject" zum Senden</span><span class="sxs-lookup"><span data-stu-id="88012-178">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





