---
title: EMailDatenbankobjekt-Makroaktion
TOCTitle: EMailDatabaseObject Macro Action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 79b903f63ba0a9b8e6fd1adf9e5a29dab9de9edb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473010"
---
# <a name="emaildatabaseobject-macro-action"></a>EMailDatenbankobjekt-Makroaktion

**Gilt für:** Access 2013 | Office 2013

Verwenden Sie die **EMailDatenbankobjekt** -Aktion, um ein angegebenes Datenblatt, ein Formular, einen Bericht, ein Modul oder eine Datenzugriffsseite von Microsoft Access zum Anzeigen oder Weiterleiten in eine E-Mail-Nachricht einzuschließen.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.

## <a name="settings"></a>Einstellungen

Die **EMailDatenbankobjekt** -Aktion hat die folgenden Argumente.

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
<td><p>Der in die E-Mail-Nachricht einzuschließende Objekttyp. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle (für ein Tabellendatenblatt), auf Abfrage (für ein Abfragedatenblatt), auf Formular (für ein Formular oder Formulardatenblatt), auf Bericht, auf Modul oder auf Datenzugriffsseite, auf Serversicht, auf Gespeicherte Prozedur oder auf Funktion. Sie können kein Makro senden. Wenn Sie das aktive Objekt einschließen möchten, wählen Sie dessen Typ mit diesem Argument aus, lassen Sie jedoch das Argument Objektname leer.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des Objekts, das zu der E-Mail hinzugefügt werden soll. Das Feld <strong>Objektname</strong> zeigt alle Objekte in der Datenbank vom Typ, der im <strong>Objekttyp</strong> -Argument ausgewählt ist. Wenn Sie die Argumente <strong>Objekttyp</strong> und <strong>Objektname</strong> leer lassen, sendet Access eine Nachricht an die E-Mail-Anwendung ohne ein Datenbankobjekt. Wenn Sie ein Makro mit der <strong>EMailDatenbankobjekt</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Access nach dem Objekt mit diesem Namen zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Ausgabeformat</strong></p></td>
<td><p>Der Typ des Formats soll für das eingeschlossene Objekt verwendet. Je nachdem, was Sie für das Argument <strong>Objekttyp</strong> auswählen ändert sich die Liste der Formate, die, denen Sie auswählen können. <strong>Excel 97 - 2003-Arbeitsmappe (*.xls)</strong>, <strong>Excel-Binärarbeitsmappe (.xlsb)</strong>, <strong>Excel-Arbeitsmappe (*.xlsx)</strong>verfügbaren Formate gehören <strong>HTML (*.htm, * .html)</strong>, <strong>Microsoft Excel 5.0/95-Arbeitsmappe (*.xls)</strong>, <strong>PDF-Format </strong>, <strong>Dialog: Rich Text Format (*.RTF)</strong>, <strong>Textdateien (*.txt)</strong>oder <strong>XPS-Format (*.XPS)</strong>. im Feld <strong>Ausgabeformat</strong> . Module können nur im Textformat gesendet werden. Datenzugriffsseiten können nur im HTML-Format gesendet werden. Wenn Sie dieses Argument leer lassen, werden Sie von Access zur Angabe eines Dateiformats aufgefordert.</p></td>
</tr>
<tr class="even">
<td><p><strong>An</strong></p></td>
<td><p>Die Empfänger der Nachricht, deren Namen in das Feld <strong>An</strong> der E-Mail-Nachricht aufgenommen werden sollen. Wenn Sie dieses Argument leer lassen, werden Sie von Access aufgefordert, die Namen der Empfänger anzugeben. Die Empfängernamen in diesem Argument 8sowie in den Argumenten <strong>Cc</strong> und <strong>Bcc</strong>) müssen durch Semikolons (;) oder durch das Listentrennzeichen voneinander getrennt werden, das in der Microsoft Windows- <strong>Systemsteuerung</strong> im Dialogfeld <strong>Ländereinstellungen</strong> auf der Registerkarte <strong>Zahlen</strong> festgelegt ist. Wenn die Empfängernamen nicht von der E-Mail-Anwendung erkannt werden, wird die Nachricht nicht gesendet, und es tritt ein Fehler auf.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Cc</strong></p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie in der <strong>Cc</strong> aufnehmen möchten (&quot;Carbon Copy, Blindkopie&quot;) Zeile in der e-Mail-Nachricht. Wenn Sie dieses Argument leer lassen, bleibt die <strong>Cc</strong>-Zeile der E-Mail-Nachricht leer.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bcc</strong></p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie in der <strong>Bcc</strong> aufnehmen möchten (&quot;blind Carbon Copy, Blindkopie&quot;) Zeile in der e-Mail-Nachricht. Wenn Sie dieses Argument leer lassen, bleibt die <strong>Bcc</strong>-Zeile der E-Mail-Nachricht leer.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Betreff</strong></p></td>
<td><p>Der Betreff der Nachricht. Dieser Text wird in der <strong>Betreff</strong>-Zeile der E-Mail-Nachricht angezeigt. Wenn Sie dieses Argument leer lassen, bleibt die <strong>Betreff</strong>-Zeile der E-Mail-Nachricht leer.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nachrichtentext</strong></p></td>
<td><p>Beliebiger Text, den Sie zusätzlich in das Datenbankobjekt einschließen möchten. Dieser Text wird im Hauptteil der E-Mail-Nachricht nach dem Objekt angezeigt. Wenn Sie dieses Argument leer lassen, wird kein zusätzlicher Text in die E-Mail-Nachricht eingeschlossen. Lassen Sie die Argumente <strong>Objekttyp</strong> und <strong>Objektname</strong> leer, können Sie mit diesem Argument eine E-Mail-Nachricht ohne Datenbankobjekt senden.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nachricht bearbeiten</strong></p></td>
<td><p>Gibt an, ob die Nachricht vor dem Senden bearbeitet werden kann. Wenn Sie <strong>Ja</strong> auswählen, wird die E-Mail-Anwendung automatisch gestartet, und die Nachricht kann bearbeitet werden. Wenn Sie <strong>Nein</strong> auswählen, wird die Nachricht gesendet, ohne dass der Benutzer eine Möglichkeit zur Bearbeitung hat. Die Standardeinstellung ist <strong>Ja</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Vorlagedatei</strong></p></td>
<td><p>Der Pfad und Dateiname einer Datei, die Sie als Vorlage für eine HTML-Datei verwenden möchten. Eine Vorlagedatei enthält HTML-Tags.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Das Objekt in der E-Mail-Nachricht ist das ausgewählte Ausgabeformat. Beim Doppelklicken auf das Objekt wird die entsprechende Software gestartet und das Objekt geöffnet.

Die folgenden Regeln gelten bei der Verwendung der **EMailDatenbankobjekt** -Aktion zum Einschließen eines Datenbankobjekts in eine E-Mail-Nachricht:

- Sie können Tabellen-, Abfrage- und Formulardatenblätter senden. Im verwendeten Objekt sehen alle Felder im Datenblatt so aus wie in Access, mit Ausnahme der Felder, die OLE-Objekte enthalten. Die Spalten für diese Felder sind im Objekt eingeschlossen, die Felder sind jedoch leer.

- Für ein Steuerelement, das an ein Ja/Nein-Feld (eine Umschaltfläche, eine Optionsschaltfläche oder ein Kontrollkästchen) gebunden ist, wird in der Ausgabedatei der Wert –1 (Ja) oder 0 (Nein) angezeigt.

- Für ein Textfeld, das an ein Hyperlink-Feld gebunden ist, wird in der Ausgabedatei der Hyperlink für alle Ausgabeformate mit Ausnahme von MS-DOS-Text angezeigt (in diesem Fall wird der Hyperlink nur als normaler Text angezeigt).

- Wenn Sie ein Formular in der Formularansicht senden, enthält das eingeschlossene Objekt immer die Datenblattansicht des Objekts.

- Wenn Sie einen Bericht senden, sind Textfelder und (in einigen Fällen) Bezeichnungsfelder die einzigen Steuerelemente, die in das Objekt eingeschlossen werden. Alle sonstigen Steuerelemente werden ignoriert. Auch Kopf- und Fußzeileninformationen werden ausgeschlossen. Die einzige Ausnahme besteht darin, dass beim Senden eines Berichts im Excel-Format ein Textfeld in einem Gruppenfuß, das einen Ausdruck mit der **Summe** -Funktion enthält, in das Objekt eingeschlossen wird. Keine anderen Steuerelemente in einer Kopf- oder Fußzeile (und keine andere Aggregatfunktion als **Summe**) werden in das Objekt eingeschlossen.

- Unterberichte sind im Objekt eingeschlossen.

- Wenn Sie ein Datenblatt, ein Formular oder eine Datenzugriffsseite im HTML-Format senden, wird eine HTML-Datei erstellt. Wenn Sie einen Bericht im HTML-Format senden, wird für jede Seite im Bericht eine HTML-Datei erstellt.

Verwenden Sie die **SendObject** -Methode des **DoCmd** -Objekts, um die **EMailDatenbankobjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

### <a name="about-the-contributor"></a>Über den Autor

**Verknüpfung von bereitgestellt.** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), Gründer und Präsident von FMS, Inc., dem führenden Anbieter von kundendatenbanklösungen und Entwickler-Tools.

  - [Merkmale und Begrenzungen in Bezug auf die Verwendung der Methode „SendObject" zum Senden](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





