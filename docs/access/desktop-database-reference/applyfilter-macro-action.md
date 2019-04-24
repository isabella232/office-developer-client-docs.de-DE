---
title: ApplyFilter-Makroaktion
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296997"
---
# <a name="applyfilter-macro-action"></a>ApplyFilter-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **AnwendenFilter** -Aktion verwenden, um einen Filter, eine Abfrage oder eine SQL WHERE-Klausel auf eine Tabelle, ein Formular oder einen Bericht anzuwenden, wenn Sie die Datensätze in der Tabelle bzw. die Datensätze der zugrunde liegenden Tabelle oder Abfrage des Formulars oder Berichts einschränken oder sortieren möchten. Für Berichte können Sie diese Aktion nur in einem Makro verwenden, das in der **BeimÖffnen** -Ereigniseigenschaft des Berichts angegeben ist.

> [!NOTE]
> [!HINWEIS] Sie können diese Aktion zum Anwenden einer SQL WHERE-Klausel nur dann verwenden, wenn Sie einen Serverfilter anwenden. Ein Serverfilter kann nicht auf die gespeicherte Datensatzquelle einer Prozedur angewendet werden.

## <a name="setting"></a>Einstellung

Die **AnwendenFilter**-Aktion hat die folgenden Argumente.

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
<td><p>Filtername</p></td>
<td><p>Der Name eines Filters oder einer Abfrage, der die Datensätze der Tabelle, des Formulars oder Berichts einschränkt oder sortiert. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als Abfrage gespeichert wurde, im Feld <strong>Filtername</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> eingeben.</p><p><strong>Hinweis</strong>: Wenn Sie diese Aktion verwenden, um einen Serverfilter anzuwenden, muss das Argument Filter Name leer sein.</p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE) oder ein Ausdruck, der die Datensätze der Tabelle, des Formulars oder des Berichts einschränkt.</p>
<p><b>Hinweis</b>: in einem WHERE-Bedingungs Argument Ausdruck enthält die linke Seite des Ausdrucks in der Regel einen Feldnamen aus der zugrunde liegenden Tabelle oder Abfrage für das Formular oder den Bericht. Die Rechte Seite des Ausdrucks enthält normalerweise die Kriterien, die Sie auf dieses Feld anwenden möchten, um die Datensätze einzuschränken oder zu sortieren. Beispielsweise können die Kriterien der Name eines Steuerelements in einem anderen Formular sein, das den Wert enthält, den die Datensätze im ersten Formular übereinstimmen sollen. Der Name des Steuerelements sollte vollständig qualifiziert sein, zum Beispiel:</p>
<p><strong>Formulare</strong>! <em>Formularname</em>! <em>Steuer Elementname</em> Feldnamen müssen in doppelte Anführungszeichen eingeschlossen werden, und Zeichenfolgenliterale sollten in einfache Anführungszeichen eingeschlossen werden. Das Argument Where Condition darf maximal 255 Zeichen enthalten. Verwenden Sie die <strong>ApplyFilter</strong>-Methode des <strong>DoCmd</strong>-Objekts in einem VBA-Modul (Visual Basic für Applikationen), wenn Sie eine längere SQL WHERE-Klausel eingeben müssen. Sie können SQL WHERE-Klauselanweisungen in VBA mit bis zu 32.768 Zeichen eingeben.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!HINWEIS] Sie können das Argument Filtername verwenden, wenn Sie bereits einen Filter definiert haben, der die entsprechenden Daten bereitstellt. Mit dem Argument "WhereCondition" können Sie die Eingrenzungskriterien direkt eingeben. Wenn Sie beide Argumente verwenden, wendet Microsoft Office Access 2007 die WHERE-Klausel auf die Ergebnisse des Filtervorgangs an. Sie müssen mindestens eines der Argumente verwenden.

## <a name="remarks"></a>Bemerkungen

Sie können einen Filter oder eine Abfrage auf ein Formular in der Formularansicht oder in der Datenblattansicht anwenden.

Der angewendete Filter und die WHERE-Bedingung werden zur Einstellung der **Filter**- oder **Serverfilter**-Eigenschaft des Formulars oder des Berichts.

Für Tabellen und Formulare ist diese Aktion mit dem Klicken auf **Filter/Sortierung anwenden** oder **Serverfilter anwenden** im Menü **Datensätze** vergleichbar. Der Menübefehl wendet den zuletzt erstellten Filter auf die Tabelle oder das Formular an, wohingegen die **AnwendenFilter** -Aktion einen angegebenen Filter oder eine angegebene Abfrage anwendet.

In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.

To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).

Beim Speichern einer Tabelle oder eines Formulars speichert Access alle Filter, die in dem Objekt derzeit definiert sind, wendet die Filter jedoch das nächste Mal, wenn das Objekt geöffnet wird, nicht an (wobei jedoch eine vor dem Speichern auf das Objekt angewendete Sortierung automatisch angewendet wird). Wenn ein Filter automatisch beim ersten Öffnen des Formulars angewendet werden soll, geben Sie ein Makro, das die **AnwendenFilter**-Aktion enthält, oder eine Ereignisprozedur mit der **ApplyFilter**-Methode des **DoCmd**-Objekts als Einstellung für die **BeimÖffnen**-Ereigniseigenschaft des Formulars an. Sie können einen Filter auch anwenden, indem Sie die **ÖffnenFormular**- oder die **ÖffnenBericht**-Aktion oder die entsprechenden Methoden verwenden. Sie können die Tabelle öffnen, indem Sie ein Makro, das die **ÖffnenTabelle**-Aktion enthält, und anschließend die **AnwendenFilter**-Aktion verwenden. Auf diese Weise wird ein Filter automatisch beim ersten Öffnen einer Tabelle angewendet.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die ApplyFilter-Aktion verwenden, um das frmFoods-Formular beim Öffnen zu filtern.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



