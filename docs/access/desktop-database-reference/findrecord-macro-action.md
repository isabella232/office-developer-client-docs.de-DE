---
title: FindRecord-Makroaktion
TOCTitle: FindRecord macro action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 47d63dd88226d74b1138b59ce441efc0ef4ce588
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622256"
---
# <a name="findrecord-macro-action"></a>FindRecord-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **SuchenDatensatz** -Aktion suchen Sie die erste Instanz der Daten, die den in den Argumenten von **SuchenDatensatz** angegebenen Kriterien entsprechen. Diese Daten können sich in dem aktuellen Datensatz, einem nachfolgenden oder früheren Datensatz oder dem ersten Datensatz befinden. Sie können Datensätze in dem aktiven Datenblatt, dem Abfragedatenblatt, dem Formulardatenblatt oder dem Formular suchen.

## <a name="setting"></a>Einstellung

Die **SuchenDatensatz**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Suchen nach</strong></p></td>
<td><p>Gibt die Daten an, die Sie im Datensatz suchen möchten. Geben Sie den Text, die Nummer oder das Datum, den Sie suchen möchten, oder geben Sie einen Ausdruck ein, dem ein Gleichheitszeichen ( ) vorangestellt ist, <strong>=</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" im Feld <strong>"Suchen nach".</strong> Sie können Platzhalterzeichen verwenden. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Match</strong></p></td>
<td><p>Gibt an, wo sich die Daten in dem Feld befinden. Sie können eine Suche für Daten in einem beliebigem Teil des Felds (<strong>Teil des Feldinhaltes</strong>), für Daten, die das ganze Feld ausfüllen (<strong>Ganzes Feld</strong>), oder für Daten, die sich am Anfang des Felds befinden (<strong>Anfang des Feldinhaltes</strong>), angeben. Die Standardeinstellung ist <strong>Ganzes Feld</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Groß-/Kleinschreibung beachten</strong></p></td>
<td><p>Gibt an, ob bei der Suche die Groß- und Kleinschreibung beachtet wird. Klicken Sie auf <strong>Ja</strong> (Suche mit Beachtung der Groß- und Kleinschreibung) oder auf <strong>Nein</strong> (Suche ohne Beachtung der genauen Groß- und Kleinschreibung). Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Search</strong></p></td>
<td><p>Gibt an, ob die Suche vom aktuellen Datensatz nach oben bis zum Anfang der Datensätze (<strong>Aufwärts</strong>), nach unten bis zum Ende der Datensätze (<strong>Abwärts</strong>) oder bis zum Ende der Datensätze und weiter vom Anfang der Datensätze bis zum aktuellen Datensatz fortfährt, sodass letztlich alle Datensätze durchsucht wurden (<strong>Alle</strong>). Die Standardeinstellung ist <strong>Alle</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Wie formatiert</strong></p></td>
<td><p>Gibt an, ob die Suche formatierte Daten einschließt. Klicken Sie auf <strong>Ja</strong> (Microsoft Office Access 2007 sucht nach den Daten, wie sie im Feld formatiert sind und angezeigt werden) oder auf <strong>Nein</strong> (Access sucht nach den Daten, wie sie in der Datenbank gespeichert sind, was nicht immer mit der Anzeige der Daten übereinstimmt). Die Standardeinstellung ist <strong>Nein</strong>. Verwenden Sie dieses Feature, um die Suche auf Daten in einem bestimmten Format zu beschränken. Klicken Sie beispielsweise auf <strong>Ja</strong>, und geben Sie <strong>1,234</strong> für das Argument <strong>Suchen nach</strong> ein, um den Wert 1,234 in einem Feld zu suchen, das so formatiert ist, dass es Kommas enthalten kann. Klicken Sie auf <strong>Nein</strong>, wenn Sie <strong>1234</strong> eingeben möchten, um in diesem Feld nach den Daten zu suchen. Klicken Sie zum Suchen nach Datumsangaben auf <strong>"Ja",</strong> um ein Datum genau so zu finden, wie es formatiert ist, z. B. 08-July-2003. Wenn Sie auf <strong>"Nein"</strong>klicken, geben Sie das Datum für das Argument <strong>"Suchen nach",</strong> in dem Format ein, das in den regionalen Einstellungen in Windows Systemsteuerung festgelegt ist. Dieses Format wird im Feld <strong>"Kurzes Datumsformat"</strong> auf der Registerkarte <strong>"Datum"</strong> in den Landes- und Regionaleinstellungen angezeigt. Wenn z. B. das Feld für das <strong>kurze Datumsformat</strong> auf <strong>M/d/yy</strong>festgelegt ist, können Sie 7/8/03 eingeben, und Access sucht alle Einträge in einem Datumsfeld, das dem 8. Juli 2003 entspricht, unabhängig davon, wie dieses Feld formatiert ist.</p>
<p><strong>HINWEIS:</strong>Das Argument <strong>"Search As Formatted"</strong> wird nur wirksam, wenn das aktuelle Feld ein gebundenes Steuerelement ist, das Argument <strong>"Match"</strong> auf <strong>"Whole Field"</strong>festgelegt ist, das Argument <strong>"Only Current Field"</strong> auf <strong>"Yes"</strong>und das Argument <strong>"Match Case"</strong> auf <strong>"No"</strong>festgelegt ist.</p>
<p>Wenn Sie <strong>Groß-/Kleinschreibung beachten</strong> auf <strong>Ja</strong> oder <strong>Nur aktuelles Feld</strong> auf <strong>Nein</strong> festlegen, müssen Sie außerdem <strong>Wie formatiert</strong> auf <strong>Ja</strong> festlegen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nur aktuelles Feld</strong></p></td>
<td><p>Gibt an, ob die Suche auf das aktuelle Feld in jedem Datensatz beschränkt wird oder ob sie alle Felder in jedem Datensatz einschließt. Die Suche im aktuellen Feld ist schneller. Klicken Sie auf <strong>Ja</strong> (beschränkt die Suche auf das aktuelle Feld) oder auf <strong>Nein</strong> (Suche in allen Feldern jedes Datensatzes). Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Am Anfang beginnen</strong></p></td>
<td><p>Gibt an, ob die Suche beim ersten Datensatz oder beim aktuellen Datensatz beginnt. Klicken Sie auf <strong>Ja</strong> (Start beim ersten Datensatz) oder auf <strong>Nein</strong> (Start beim aktuellen Datensatz). Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn ein Makro die **SuchenDatensatz** -Aktion ausführt, sucht Access nach den angegebenen Daten in den Datensätzen (die Reihenfolge der Suche wird durch die Einstellung des Arguments **Suchen** bestimmt). Kann Access die angegebenen Daten finden, sind die Daten im Datensatz markiert.

The **FindRecord** action is equivalent to clicking **Find** on the **Home** tab, and its arguments are the same as the options in the **Find and Replace** dialog box. If you set the **FindRecord** arguments in the Macro Builder pane and then run the macro, you will see the corresponding options selected in the **Find and Replace** dialog box when you click **Find**.

Access behält während einer Datenbanksitzung die letzten Argumente von **SuchenDatensatz** bei, sodass Sie dieselben Kriterien nicht erneut eingeben müssen, wenn Sie nachfolgend Vorgänge mit der **SuchenDatensatz** -Aktion ausführen. Wenn Sie ein Argument leer lassen, verwendet Access die letzte Einstellung für das Argument, basierend auf der vorherigen **SuchenDatensatz** -Aktion oder der Einstellung im Dialogfeld **Suchen und Ersetzen**.

Wenn Sie einen Datensatz mithilfe eines Makros finden möchten, sollten Sie die **SuchenDatensatz** -Aktion verwenden. Verwenden Sie nicht die **AusführenMenübefehl** -Aktion, deren Argument so festgelegt ist, dass der Befehl **Suchen** ausgeführt wird.

> [!NOTE]
> [!HINWEIS] Die **SuchenDatensatz** -Aktion entspricht zwar dem Befehl **Suchen** auf der Registerkarte **Start** für Tabellen, Abfragen und Formulare, sie entspricht jedoch nicht dem Befehl **Suchen** im Menü **Bearbeiten** im Codefenster. Um nach Text in Modulen zu suchen, können Sie die **SuchenDatensatz** -Aktion nicht verwenden.

Wenn der aktuell ausgewählte Text zu dem Zeitpunkt, zu dem die **SuchenDatensatz** -Aktion ausgeführt wird, mit dem Suchtext übereinstimmt, beginnt die Suche sofort im Anschluss an die Auswahl in demselben Feld wie die Auswahl und in demselben Datensatz. Andernfalls beginnt die Suche am Anfang des aktuellen Datensatzes. Hierdurch ist es Ihnen möglich, mehrere Instanzen derselben Suchkriterien zu finden, die in einem einzelnen Datensatz enthalten sein können.

Beachten Sie jedoch Folgendes: Wenn Sie eine Befehlsschaltfläche zum Ausführen eines Makros verwenden, das die **SuchenDatensatz** -Aktion enthält, wird immer wieder das erste Vorkommen der Suchkriterien gefunden. Dieses Verhalten tritt auf, da durch Klicken auf die Befehlsschaltfläche der Fokus aus dem Feld entfernt wird, das den zu suchenden Wert enthält. Die **SuchenDatensatz** -Aktion beginnt daraufhin mit der Suche am Anfang des Datensatzes. Sie können das Problem vermeiden, indem Sie das Makro mithilfe eines Verfahrens ausführen, durch das der Fokus nicht verschoben wird, z. B. eine benutzerdefinierte Symbolleistenschaltfläche oder eine Tastenkombination, die in einem AutoKeys-Makro festgelegt ist, oder indem Sie den Fokus im Makro auf das Feld festlegen, das die Suchkriterien enthält, bevor Sie die **SuchenDatensatz** -Aktion ausführen.

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><strong>Sicherheitshinweis</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vermeiden Sie die <strong>SendKeys</strong>-Anweisung oder ein AutoKeys-Makro mit sensiblen oder vertraulichen Informationen. Ein böswilliger Benutzer kann die Tastatureingaben abfangen und die Sicherheit von Computer und Daten gefährden.</td>
</tr>
</tbody>
</table>

Dasselbe Verhalten tritt auf, wenn Sie eine Befehlsschaltfläche verwenden, um ein Makro auszuführen, das die **SuchenWeiter** -Aktion enthält.

Verwenden Sie die **SuchenDatensatz** -Methode des **DoCmd** -Objekts, um die **SuchenDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

Für komplexere Suchvorgänge ist es empfehlenswert, die **SuchenNachDatensatz** -Makroaktion zu verwenden.

