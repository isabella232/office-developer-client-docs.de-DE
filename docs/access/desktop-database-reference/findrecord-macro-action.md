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
ms.openlocfilehash: 74d3c050b7d3912c6b0b369f99ca163cee87643a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919710"
---
# <a name="findrecord-macro-action"></a>FindRecord-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **SuchenDatensatz** -Aktion suchen Sie die erste Instanz der Daten, die den in den Argumenten von **SuchenDatensatz** angegebenen Kriterien entsprechen. Diese Daten können sich in dem aktuellen Datensatz, einem nachfolgenden oder früheren Datensatz oder dem ersten Datensatz befinden. Sie können Datensätze in dem aktiven Datenblatt, dem Abfragedatenblatt, dem Formulardatenblatt oder dem Formular suchen.

## <a name="setting"></a>Einstellung

Die **SuchenDatensatz** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Suchen</strong></p></td>
<td><p>Gibt an, die Daten, die im Datensatz ermittelt werden soll. Geben Sie den Text, Zahl oder Datum, die Sie suchen möchten oder einen Ausdruck, dem ein Gleichheitszeichen vorangestellt wird (<strong>=</strong>), in das Feld <strong>Suchen nach</strong> im <strong>Abschnitt</strong> Bereich des Makro-Generators. Sie können Platzhalterzeichen verwenden. Dies ist ein erforderliches Argument.</p></td>
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
<td><p><strong>Suchen</strong></p></td>
<td><p>Gibt an, ob die Suche vom aktuellen Datensatz nach oben bis zum Anfang der Datensätze (<strong>Aufwärts</strong>), nach unten bis zum Ende der Datensätze (<strong>Abwärts</strong>) oder bis zum Ende der Datensätze und weiter vom Anfang der Datensätze bis zum aktuellen Datensatz fortfährt, sodass letztlich alle Datensätze durchsucht wurden (<strong>Alle</strong>). Die Standardeinstellung ist <strong>Alle</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Wie formatiert</strong></p></td>
<td><p>Gibt an, ob die Suche formatierte Daten enthält. Klicken Sie auf <strong>Ja</strong> (Microsoft Office Access 2007 sucht sich nach den Daten, wie sie formatiert und im Feld angezeigt wird) oder auf <strong>Nein</strong> (Access sucht nach Daten an, in der Datenbank gespeichert wird, die nicht immer die gleichen wie es angezeigt wird). Die Standardeinstellung ist <strong>Nein</strong>. Dieses Feature können Sie um die Suche auf Daten in einem bestimmten Format zu beschränken. Angenommen, klicken Sie auf <strong>Ja</strong> , und geben Sie <strong>1,234</strong> in das Argument <strong>Suchen</strong> nach einem 1,234 in einem Feld so formatiert, dass Kommas enthalten. Klicken Sie auf <strong>Nein</strong> , wenn Sie <strong>1234</strong> für die Daten in diesem Feld Suchen eingeben möchten. Um nach Datumsangaben zu suchen, klicken Sie auf <strong>Ja,</strong> um ein Datum zu suchen, genau wie, beispielsweise 08 Juli 2003 formatiert. Klicken Sie auf <strong>Nein</strong>, geben Sie das Datum für das Argument <strong>Suchen nach</strong> im Format, das in den regionalen Einstellungen in Windows-Systemsteuerung festgelegt ist. Dieses Format ist im <strong>kurzen Datumsformat</strong> finden Sie auf der Registerkarte <strong>Datum</strong> in den regionalen Einstellungen angezeigt. Angenommen, wenn das Feld <strong>kurzen Datumsformat</strong> auf <strong>m/JJ</strong>festgelegt ist, können Sie 7/8/03 eingeben und Access findet alle Einträge in einem Datumsfeld, die entsprechen, 8. Juli 2003, unabhängig davon, wie das Feld formatiert ist.</p>

> [!NOTE]
> <P>Das Argument <STRONG>Wie formatiert</STRONG> ist nur dann wirksam, wenn das aktuelle Feld ein gebundenes Steuerelement ist und wenn das Argument <STRONG>Vergleichen</STRONG> auf <STRONG>Ganzes Feld</STRONG>, das Argument <STRONG>Nur aktuelles Feld</STRONG> auf <STRONG>Ja</STRONG> und das Argument <STRONG>Groß-/Kleinschreibung beachten</STRONG> auf <STRONG>Nein</STRONG> festgelegt ist.</P>


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


## <a name="remarks"></a>Hinweise

Wenn ein Makro die **SuchenDatensatz** -Aktion ausführt, sucht Access nach den angegebenen Daten in den Datensätzen (die Reihenfolge der Suche wird durch die Einstellung des Arguments **Suchen** bestimmt). Kann Access die angegebenen Daten finden, sind die Daten im Datensatz markiert.

Die SuchenDatensatz-Aktion hat dieselbe Wirkung wie das Klicken auf Suchen auf der Registerkarte Daten. Die Argumente stimmen mit den Optionen im Dialogfeld Suchen und Ersetzen überein. Wenn Sie die Argumente für SuchenDatensatz im Bereich Makro-Generator festlegen und das Makro dann ausführen, werden die entsprechenden Optionen im Dialogfeld Suchen und Ersetzen aktiviert anzeigt, sobald Sie auf Suchen klicken.

Access behält während einer Datenbanksitzung die letzten Argumente von **SuchenDatensatz** bei, sodass Sie dieselben Kriterien nicht erneut eingeben müssen, wenn Sie nachfolgend Vorgänge mit der **SuchenDatensatz** -Aktion ausführen. Wenn Sie ein Argument leer lassen, verwendet Access die letzte Einstellung für das Argument, basierend auf der vorherigen **SuchenDatensatz** -Aktion oder der Einstellung im Dialogfeld **Suchen und Ersetzen**.

Wenn Sie einen Datensatz mithilfe eines Makros finden möchten, sollten Sie die **SuchenDatensatz** -Aktion verwenden. Verwenden Sie nicht die **AusführenMenübefehl** -Aktion, deren Argument so festgelegt ist, dass der Befehl **Suchen** ausgeführt wird.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>SuchenDatensatz</STRONG> -Aktion entspricht zwar dem Befehl <STRONG>Suchen</STRONG> auf der Registerkarte <STRONG>Start</STRONG> für Tabellen, Abfragen und Formulare, sie entspricht jedoch nicht dem Befehl <STRONG>Suchen</STRONG> im Menü <STRONG>Bearbeiten</STRONG> im Codefenster. Um nach Text in Modulen zu suchen, können Sie die <STRONG>SuchenDatensatz</STRONG> -Aktion nicht verwenden.</P>



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
<td>
      Vermeiden Sie bei sensiblen oder vertraulichen Informationen die Verwendung der <strong>SendKeys</strong>-Anweisung oder eines AutoKeys-Makros. Ein bösartiger Benutzer könnte die Tastenfolgen abfangen und die Sicherheit Ihres Computers und Ihrer Daten gefährden.
</td>
</tr>
</tbody>
</table>


Dasselbe Verhalten tritt auf, wenn Sie eine Befehlsschaltfläche verwenden, um ein Makro auszuführen, das die **SuchenWeiter** -Aktion enthält.

Verwenden Sie die **SuchenDatensatz** -Methode des **DoCmd** -Objekts, um die **SuchenDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

Für komplexere Suchvorgänge ist es empfehlenswert, die **SuchenNachDatensatz** -Makroaktion zu verwenden.

