---
title: GoToRecord-Makroaktion
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708480"
---
# <a name="gotorecord-macro-action"></a>GoToRecord-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **GeheZuDatensatz** -Aktion können Sie den angegebenen Datensatz zum aktuellen Datensatz in einer geöffneten Tabelle oder einem geöffneten Formular oder Abfrageresultset machen.

## <a name="setting"></a>Einstellung

Die **GeheZuDatensatz** -Aktion hat die folgenden Argumente.

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
<td><p>Der Typ des Objekts, das den Datensatz enthält, den Sie zum aktuellen Datensatz machen möchten. Klicken Sie auf Tabelle, auf Abfrage, auf Formular, auf Serversicht, auf Gespeicherte Prozedur oder auf Funktion im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator. Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des Objekts, das den Datensatz enthält, den sie zum aktuellen Datensatz machen möchten. Im Feld <strong>Objektname</strong> werden alle Objekte in der aktuellen Datenbank angezeigt, die den durch das Argument <strong>Objekttyp</strong> angegebenen Typ aufweisen. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Der Datensatz, der zum aktuellen Datensatz werden soll. Klicken Sie im Feld <strong>Datensatz</strong> auf <strong>Vorheriger</strong>, <strong>Nächster</strong>, <strong>Erster</strong>, <strong>Letzter</strong>, <strong>Gehe zu</strong> oder <strong>Neu</strong>. Die Standardeinstellung ist <strong>Nächster</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Eine ganze Zahl oder ein Ausdruck, der eine ganze Zahl ausgewertet wird. Ein Ausdruck muss ein Gleichheitszeichen vorangestellt werden (<strong>=</strong>). Dieses Argument gibt den Datensatz zum aktuellen Datensatz machen. Sie können das Argument <strong>Offset</strong> auf zwei Arten verwenden:</p>
<ul>
<li><p>Wenn das Argument <strong>Datensatz</strong> auf <strong>Nächster</strong> oder <strong>Vorheriger</strong> festgelegt ist, verschiebt Microsoft Office Access 2007 den Fokus um die Anzahl von Datensätzen nach vorn oder hinten, die im Argument <strong>Offset</strong> angegeben ist.</p></li>
<li><p>Wenn das Argument <strong>Datensatz</strong> auf <strong>Gehe zu</strong> festgelegt ist, wechselt Access zu dem Datensatz mit der Nummer, die dem Argument <strong>Offset</strong> entspricht. Die Datensatznummer wird im Datensatznummernfeld am unteren Rand des Fensters angezeigt.</p>
<p><strong>Hinweis</strong>: Wenn Sie die <strong>ersten</strong>, <strong>letzten</strong>oder <strong>neue</strong> Einstellung für das Argument <strong>Datensatz</strong> verwenden, ignoriert Access das Argument <strong>Offset</strong> . Wenn Sie ein Argument <strong>Offset</strong> , die zu groß ist eingeben, wird von Access eine Fehlermeldung angezeigt. Sie können nicht negative Zahlen für das Argument <strong>Offset</strong> eingeben.</p></li>
<li><p>Wenn das Argument <strong>Datensatz</strong> auf <strong>Nächster</strong> oder <strong>Vorheriger</strong> festgelegt ist, verschiebt Microsoft Office Access 2007 den Fokus um die Anzahl von Datensätzen nach vorn oder hinten, die im Argument <strong>Offset</strong> angegeben ist.</p></li>
<li><p>Wenn das Argument <strong>Datensatz</strong> auf <strong>Gehe zu</strong> festgelegt ist, wechselt Access zu dem Datensatz mit der Nummer, die dem Argument <strong>Offset</strong> entspricht. Die Datensatznummer wird im Datensatznummernfeld am unteren Rand des Fensters angezeigt.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn sich der Fokus in einem bestimmten Steuerelement in einem Datensatz befindet, belässt diese Aktion den Fokus im selben Steuerelement für den neuen Datensatz.

Sie können die Einstellung **Neu** für das Argument **Datensatz** verwenden, um sich zum leeren Datensatz am Ende eines Formulars oder einer Tabelle zu bewegen, sodass Sie neue Daten eingeben können.

Diese Aktion ist mit dem Klicken auf den Pfeil unterhalb der Schaltfläche **Suchen** auf der Registerkarte **Start** und dem anschließenden Klicken auf **Gehe zu** vergleichbar. Die Unterbefehle **Erster**, **Letzter**, **Nächster**, **Vorheriger** und **Neuer Datensatz** des Befehls **Gehe zu** haben dieselbe Wirkung auf das ausgewählte Objekt wie die Einstellungen **Erster**, **Letzter**, **Nächster**, **Vorheriger** und **Neu** für das Argument **Datensatz**. Sie können auch zu Datensätzen wechseln, indem Sie die Navigationsschaltflächen am unteren Rand des Fensters verwenden.

Sie können die **GeheZuDatensatz** -Aktion verwenden, um einen Datensatz in einem ausgeblendeten Formular zum aktuellen Datensatz zu machen, indem Sie das ausgeblendete Formular in den Argumenten **Objekttyp** und **Objektname** angeben.

Verwenden Sie die **GoToRecord** -Methode des **DoCmd** -Objekts, um die **GeheZuDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

