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
# <a name="findrecord-macro-action"></a><span data-ttu-id="d37c1-102">FindRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="d37c1-102">FindRecord macro action</span></span>


<span data-ttu-id="d37c1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d37c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d37c1-p101">Mit der **SuchenDatensatz** -Aktion suchen Sie die erste Instanz der Daten, die den in den Argumenten von **SuchenDatensatz** angegebenen Kriterien entsprechen. Diese Daten können sich in dem aktuellen Datensatz, einem nachfolgenden oder früheren Datensatz oder dem ersten Datensatz befinden. Sie können Datensätze in dem aktiven Datenblatt, dem Abfragedatenblatt, dem Formulardatenblatt oder dem Formular suchen.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p101">You can use the **FindRecord** action to find the first instance of data that meets the criteria specified by the **FindRecord** arguments. This data can be in the current record, in a succeeding or prior record, or in the first record. You can find records in the active table datasheet, query datasheet, form datasheet, or form.</span></span>

## <a name="setting"></a><span data-ttu-id="d37c1-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d37c1-107">Setting</span></span>

<span data-ttu-id="d37c1-108">Die **SuchenDatensatz** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d37c1-108">The **FindRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d37c1-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="d37c1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d37c1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d37c1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d37c1-111"><strong>Suchen</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-111"><strong>Find What</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-112">Gibt an, die Daten, die im Datensatz ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d37c1-112">Specifies the data you want to find in the record.</span></span> <span data-ttu-id="d37c1-113">Geben Sie den Text, Zahl oder Datum, die Sie suchen möchten oder einen Ausdruck, dem ein Gleichheitszeichen vorangestellt wird (<strong>=</strong>), in das Feld <strong>Suchen nach</strong> im <strong>Abschnitt</strong> Bereich des Makro-Generators.</span><span class="sxs-lookup"><span data-stu-id="d37c1-113">Enter the text, number, or date you want to find or type an expression, which is preceded by an equal sign (<strong>=</strong>), in the <strong>Find What</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d37c1-114">Sie können Platzhalterzeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d37c1-114">You can use wildcard characters.</span></span> <span data-ttu-id="d37c1-115">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="d37c1-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37c1-116"><strong>Match</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-116"><strong>Match</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-p103">Gibt an, wo sich die Daten in dem Feld befinden. Sie können eine Suche für Daten in einem beliebigem Teil des Felds (<strong>Teil des Feldinhaltes</strong>), für Daten, die das ganze Feld ausfüllen (<strong>Ganzes Feld</strong>), oder für Daten, die sich am Anfang des Felds befinden (<strong>Anfang des Feldinhaltes</strong>), angeben. Die Standardeinstellung ist <strong>Ganzes Feld</strong>.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p103">Specifies where the data is located in the field. You can specify a search for data in any part of the field (<strong>Any Part of Field</strong>), for data that fills the entire field (<strong>Whole Field</strong>), or for data located at the beginning of the field (<strong>Start of Field</strong>). The default is <strong>Whole Field</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37c1-120"><strong>Groß-/Kleinschreibung beachten</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-120"><strong>Match Case</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-p104">Gibt an, ob bei der Suche die Groß- und Kleinschreibung beachtet wird. Klicken Sie auf <strong>Ja</strong> (Suche mit Beachtung der Groß- und Kleinschreibung) oder auf <strong>Nein</strong> (Suche ohne Beachtung der genauen Groß- und Kleinschreibung). Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p104">Specifies whether the search is case-sensitive. Click <strong>Yes</strong> (conduct a case-sensitive search) or <strong>No</strong> (search without matching uppercase and lowercase letters exactly). The default is <strong>No</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37c1-124"><strong>Suchen</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-124"><strong>Search</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-p105">Gibt an, ob die Suche vom aktuellen Datensatz nach oben bis zum Anfang der Datensätze (<strong>Aufwärts</strong>), nach unten bis zum Ende der Datensätze (<strong>Abwärts</strong>) oder bis zum Ende der Datensätze und weiter vom Anfang der Datensätze bis zum aktuellen Datensatz fortfährt, sodass letztlich alle Datensätze durchsucht wurden (<strong>Alle</strong>). Die Standardeinstellung ist <strong>Alle</strong>.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p105">Specifies whether the search proceeds from the current record up to the beginning of the records (<strong>Up</strong>); down to the end of the records (<strong>Down</strong>); or down to the end of the records and then from the beginning of the records to the current record, so all records are searched (<strong>All</strong>). The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37c1-127"><strong>Wie formatiert</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-127"><strong>Search As Formatted</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-128">Gibt an, ob die Suche formatierte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d37c1-128">Specifies whether the search includes formatted data.</span></span> <span data-ttu-id="d37c1-129">Klicken Sie auf <strong>Ja</strong> (Microsoft Office Access 2007 sucht sich nach den Daten, wie sie formatiert und im Feld angezeigt wird) oder auf <strong>Nein</strong> (Access sucht nach Daten an, in der Datenbank gespeichert wird, die nicht immer die gleichen wie es angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="d37c1-129">Click <strong>Yes</strong> (Microsoft Office Access 2007 searches for the data as it is formatted and displayed in the field) or <strong>No</strong> (Access searches for the data as it is stored in the database, which isn't always the same as it's displayed).</span></span> <span data-ttu-id="d37c1-130">Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="d37c1-130">The default is <strong>No</strong>.</span></span> <span data-ttu-id="d37c1-131">Dieses Feature können Sie um die Suche auf Daten in einem bestimmten Format zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="d37c1-131">You can use this feature to restrict the search to data in a particular format.</span></span> <span data-ttu-id="d37c1-132">Angenommen, klicken Sie auf <strong>Ja</strong> , und geben Sie <strong>1,234</strong> in das Argument <strong>Suchen</strong> nach einem 1,234 in einem Feld so formatiert, dass Kommas enthalten.</span><span class="sxs-lookup"><span data-stu-id="d37c1-132">For example, click <strong>Yes</strong> and type <strong>1,234</strong> in the <strong>Find What</strong> argument to find a value of 1,234 in a field formatted to include commas.</span></span> <span data-ttu-id="d37c1-133">Klicken Sie auf <strong>Nein</strong> , wenn Sie <strong>1234</strong> für die Daten in diesem Feld Suchen eingeben möchten.</span><span class="sxs-lookup"><span data-stu-id="d37c1-133">Click <strong>No</strong> if you want to type <strong>1234</strong> to search for the data in this field.</span></span> <span data-ttu-id="d37c1-134">Um nach Datumsangaben zu suchen, klicken Sie auf <strong>Ja,</strong> um ein Datum zu suchen, genau wie, beispielsweise 08 Juli 2003 formatiert.</span><span class="sxs-lookup"><span data-stu-id="d37c1-134">To search for dates, click <strong>Yes</strong> to find a date exactly as it is formatted, such as 08-July-2003.</span></span> <span data-ttu-id="d37c1-135">Klicken Sie auf <strong>Nein</strong>, geben Sie das Datum für das Argument <strong>Suchen nach</strong> im Format, das in den regionalen Einstellungen in Windows-Systemsteuerung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d37c1-135">If you click <strong>No</strong>, enter the date for the <strong>Find What</strong> argument in the format that is set in the regional settings in Windows Control Panel.</span></span> <span data-ttu-id="d37c1-136">Dieses Format ist im <strong>kurzen Datumsformat</strong> finden Sie auf der Registerkarte <strong>Datum</strong> in den regionalen Einstellungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d37c1-136">This format is shown in the <strong>Short date format</strong> box found on the <strong>Date</strong> tab in the regional settings.</span></span> <span data-ttu-id="d37c1-137">Angenommen, wenn das Feld <strong>kurzen Datumsformat</strong> auf <strong>m/JJ</strong>festgelegt ist, können Sie 7/8/03 eingeben und Access findet alle Einträge in einem Datumsfeld, die entsprechen, 8. Juli 2003, unabhängig davon, wie das Feld formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="d37c1-137">For example, if the <strong>Short date format</strong> box is set to <strong>M/d/yy</strong>, you can enter 7/8/03, and Access will find all entries in a Date field that correspond to July 8, 2003, regardless of how this field is formatted.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="d37c1-138">Das Argument <STRONG>Wie formatiert</STRONG> ist nur dann wirksam, wenn das aktuelle Feld ein gebundenes Steuerelement ist und wenn das Argument <STRONG>Vergleichen</STRONG> auf <STRONG>Ganzes Feld</STRONG>, das Argument <STRONG>Nur aktuelles Feld</STRONG> auf <STRONG>Ja</STRONG> und das Argument <STRONG>Groß-/Kleinschreibung beachten</STRONG> auf <STRONG>Nein</STRONG> festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d37c1-138">The <STRONG>Search As Formatted</STRONG> argument takes effect only if the current field is a bound control, the <STRONG>Match</STRONG> argument is set to <STRONG>Whole Field</STRONG>, the <STRONG>Only Current Field</STRONG> argument is set to <STRONG>Yes</STRONG>, and the <STRONG>Match Case</STRONG> argument is set to <STRONG>No</STRONG>.</span></span></P>


<p><span data-ttu-id="d37c1-139">Wenn Sie <strong>Groß-/Kleinschreibung beachten</strong> auf <strong>Ja</strong> oder <strong>Nur aktuelles Feld</strong> auf <strong>Nein</strong> festlegen, müssen Sie außerdem <strong>Wie formatiert</strong> auf <strong>Ja</strong> festlegen.</span><span class="sxs-lookup"><span data-stu-id="d37c1-139">If you set <strong>Match Case</strong> to <strong>Yes</strong> or <strong>Only Current Field</strong> to <strong>No</strong>, you must also set <strong>Search As Formatted</strong> to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37c1-140"><strong>Nur aktuelles Feld</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-140"><strong>Only Current Field</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-p107">Gibt an, ob die Suche auf das aktuelle Feld in jedem Datensatz beschränkt wird oder ob sie alle Felder in jedem Datensatz einschließt. Die Suche im aktuellen Feld ist schneller. Klicken Sie auf <strong>Ja</strong> (beschränkt die Suche auf das aktuelle Feld) oder auf <strong>Nein</strong> (Suche in allen Feldern jedes Datensatzes). Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p107">Specifies whether the search is confined to the current field in each record or includes all fields in each record. Searching in the current field is faster. Click <strong>Yes</strong> (confine the search to the current field) or <strong>No</strong> (search in all fields in each record). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37c1-145"><strong>Am Anfang beginnen</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-145"><strong>Find First</strong></span></span></p></td>
<td><p><span data-ttu-id="d37c1-p108">Gibt an, ob die Suche beim ersten Datensatz oder beim aktuellen Datensatz beginnt. Klicken Sie auf <strong>Ja</strong> (Start beim ersten Datensatz) oder auf <strong>Nein</strong> (Start beim aktuellen Datensatz). Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p108">Specifies whether the search starts at the first record or at the current record. Click <strong>Yes</strong> (start at the first record) or <strong>No</strong> (start at the current record). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d37c1-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d37c1-149">Remarks</span></span>

<span data-ttu-id="d37c1-p109">Wenn ein Makro die **SuchenDatensatz** -Aktion ausführt, sucht Access nach den angegebenen Daten in den Datensätzen (die Reihenfolge der Suche wird durch die Einstellung des Arguments **Suchen** bestimmt). Kann Access die angegebenen Daten finden, sind die Daten im Datensatz markiert.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p109">When a macro runs the **FindRecord** action, Access searches for the specified data in the records (the order of the search is determined by the setting of the **Search** argument). When Access finds the specified data, the data is selected in the record.</span></span>

<span data-ttu-id="d37c1-p110">Die SuchenDatensatz-Aktion hat dieselbe Wirkung wie das Klicken auf Suchen auf der Registerkarte Daten. Die Argumente stimmen mit den Optionen im Dialogfeld Suchen und Ersetzen überein. Wenn Sie die Argumente für SuchenDatensatz im Bereich Makro-Generator festlegen und das Makro dann ausführen, werden die entsprechenden Optionen im Dialogfeld Suchen und Ersetzen aktiviert anzeigt, sobald Sie auf Suchen klicken.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p110">The **FindRecord** action is equivalent to clicking **Find** on the **Home** tab, and its arguments are the same as the options in the **Find and Replace** dialog box. If you set the **FindRecord** arguments in the Macro Builder pane and then run the macro, you will see the corresponding options selected in the **Find and Replace** dialog box when you click **Find**.</span></span>

<span data-ttu-id="d37c1-p111">Access behält während einer Datenbanksitzung die letzten Argumente von **SuchenDatensatz** bei, sodass Sie dieselben Kriterien nicht erneut eingeben müssen, wenn Sie nachfolgend Vorgänge mit der **SuchenDatensatz** -Aktion ausführen. Wenn Sie ein Argument leer lassen, verwendet Access die letzte Einstellung für das Argument, basierend auf der vorherigen **SuchenDatensatz** -Aktion oder der Einstellung im Dialogfeld **Suchen und Ersetzen**.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p111">Access retains the most recent **FindRecord** arguments during a database session so that you don't need to enter the same criteria repeatedly as you perform subsequent operations with the **FindRecord** action. If you leave an argument blank, Access uses the most recent setting for the argument, as set either by a previous **FindRecord** action or in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="d37c1-156">Wenn Sie einen Datensatz mithilfe eines Makros finden möchten, sollten Sie die **SuchenDatensatz** -Aktion verwenden. Verwenden Sie nicht die **AusführenMenübefehl** -Aktion, deren Argument so festgelegt ist, dass der Befehl **Suchen** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d37c1-156">When you want to find a record by using a macro, use the **FindRecord** action, not the **RunMenuCommand** action with its argument set to run the **Find** command.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d37c1-p112">[!HINWEIS] Die <STRONG>SuchenDatensatz</STRONG> -Aktion entspricht zwar dem Befehl <STRONG>Suchen</STRONG> auf der Registerkarte <STRONG>Start</STRONG> für Tabellen, Abfragen und Formulare, sie entspricht jedoch nicht dem Befehl <STRONG>Suchen</STRONG> im Menü <STRONG>Bearbeiten</STRONG> im Codefenster. Um nach Text in Modulen zu suchen, können Sie die <STRONG>SuchenDatensatz</STRONG> -Aktion nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p112">While the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window. You can't use the <STRONG>FindRecord</STRONG> action to search for text in modules.</span></span></P>



<span data-ttu-id="d37c1-p113">Wenn der aktuell ausgewählte Text zu dem Zeitpunkt, zu dem die **SuchenDatensatz** -Aktion ausgeführt wird, mit dem Suchtext übereinstimmt, beginnt die Suche sofort im Anschluss an die Auswahl in demselben Feld wie die Auswahl und in demselben Datensatz. Andernfalls beginnt die Suche am Anfang des aktuellen Datensatzes. Hierdurch ist es Ihnen möglich, mehrere Instanzen derselben Suchkriterien zu finden, die in einem einzelnen Datensatz enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p113">If the currently selected text is the same as the search text at the time the **FindRecord** action is carried out, the search begins immediately following the selection in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="d37c1-p114">Beachten Sie jedoch Folgendes: Wenn Sie eine Befehlsschaltfläche zum Ausführen eines Makros verwenden, das die **SuchenDatensatz** -Aktion enthält, wird immer wieder das erste Vorkommen der Suchkriterien gefunden. Dieses Verhalten tritt auf, da durch Klicken auf die Befehlsschaltfläche der Fokus aus dem Feld entfernt wird, das den zu suchenden Wert enthält. Die **SuchenDatensatz** -Aktion beginnt daraufhin mit der Suche am Anfang des Datensatzes. Sie können das Problem vermeiden, indem Sie das Makro mithilfe eines Verfahrens ausführen, durch das der Fokus nicht verschoben wird, z. B. eine benutzerdefinierte Symbolleistenschaltfläche oder eine Tastenkombination, die in einem AutoKeys-Makro festgelegt ist, oder indem Sie den Fokus im Makro auf das Feld festlegen, das die Suchkriterien enthält, bevor Sie die **SuchenDatensatz** -Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="d37c1-p114">However, note that if you use a command button to run a macro containing the **FindRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro, or set the focus in the macro to the field containing the search criteria before you carry out the **FindRecord** action.</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><span data-ttu-id="d37c1-167"><strong>Sicherheitshinweis</strong></span><span class="sxs-lookup"><span data-stu-id="d37c1-167"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d37c1-p115">
      Vermeiden Sie bei sensiblen oder vertraulichen Informationen die Verwendung der <strong>SendKeys</strong>-Anweisung oder eines AutoKeys-Makros. Ein bösartiger Benutzer könnte die Tastenfolgen abfangen und die Sicherheit Ihres Computers und Ihrer Daten gefährden.
</span><span class="sxs-lookup"><span data-stu-id="d37c1-p115">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d37c1-170">Dasselbe Verhalten tritt auf, wenn Sie eine Befehlsschaltfläche verwenden, um ein Makro auszuführen, das die **SuchenWeiter** -Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="d37c1-170">The same behavior also occurs if you use a command button to run a macro containing the **FindNext** action.</span></span>

<span data-ttu-id="d37c1-171">Verwenden Sie die **SuchenDatensatz** -Methode des **DoCmd** -Objekts, um die **SuchenDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d37c1-171">To run the **FindRecord** action in a Visual Basic for Applications (VBA) module, use the **FindRecord** method of the **DoCmd** object.</span></span>

<span data-ttu-id="d37c1-172">Für komplexere Suchvorgänge ist es empfehlenswert, die **SuchenNachDatensatz** -Makroaktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d37c1-172">For more complex searches, you may want to use the **SearchForRecord** macro action.</span></span>

