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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716848"
---
# <a name="applyfilter-macro-action"></a>ApplyFilter-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können die **AnwendenFilter** -Aktion verwenden, um einen Filter, eine Abfrage oder eine SQL WHERE-Klausel auf eine Tabelle, ein Formular oder einen Bericht anzuwenden, wenn Sie die Datensätze in der Tabelle bzw. die Datensätze der zugrunde liegenden Tabelle oder Abfrage des Formulars oder Berichts einschränken oder sortieren möchten. Für Berichte können Sie diese Aktion nur in einem Makro verwenden, das in der **BeimÖffnen** -Ereigniseigenschaft des Berichts angegeben ist.

> [!NOTE]
> [!HINWEIS] Sie können diese Aktion zum Anwenden einer SQL WHERE-Klausel nur dann verwenden, wenn Sie einen Serverfilter anwenden. Ein Serverfilter kann nicht auf die gespeicherte Datensatzquelle einer Prozedur angewendet werden.

## <a name="setting"></a>Einstellung

Die **AnwendenFilter** -Aktion hat die folgenden Argumente.

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
<td><p>Der Name eines Filters oder einer Abfrage, die die Datensätze der Tabelle, Formular oder Bericht einschränkt oder sortiert. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, das als eine Abfrage im Feld <strong>Name des Filters</strong> im <strong>Abschnitt</strong> Bereich des <strong>Makro-Generators</strong> gespeichert wurde, eingeben.</p><p><strong>Hinweis</strong>: Wenn Sie diese Aktion verwenden, um einen Serverfilter anzuwenden, muss das Argument Filtername leer sein.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE) oder ein Ausdruck, der die Datensätze der Tabelle, des Formulars oder des Berichts einschränkt. 

</p>
<p><b>Hinweis</b>: In einer Bedingung-Argumentausdruck, der linken Seite des Ausdrucks in der Regel enthält einen Feldnamen aus der zugrunde liegenden Tabelle oder Abfrage für das Formular oder Bericht. Die rechte Seite des Ausdrucks enthält in der Regel die Kriterien, die Sie in dieses Feld einschränken oder Sortieren der Datensätze anwenden möchten. Die Kriterien können beispielsweise den Namen eines Steuerelements oder eines anderen Formulars sein, die den Wert enthält, den die Datensätze in der ersten Formular übereinstimmen sollen. Der Name des Steuerelements sollte beispielsweise vollständig qualifizierte sein:</p>
<p><strong>Formulare</strong>! <em>Formularname</em>! <em>Steuerelementname</em> Feldnamen sollten von doppelten Anführungszeichen umgeben sein und Zeichenfolgenliterale von Hochkommas umgeben sein sollte. Das Argument Bedingung die maximale Länge beträgt 255 Zeichen. Wenn Sie eine längere SQL WHERE-Klausel eingeben müssen, verwenden Sie die <strong>ApplyFilter</strong> -Methode des <strong>DoCmd</strong> -Objekts in einem Visual Basic für Applikationen (VBA)-Modul. Sie können in VBA SQL WHERE-Klausel Anweisungen von bis zu 32.768 Zeichen eingeben.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!HINWEIS] Sie können das Argument Filtername verwenden, wenn Sie bereits einen Filter definiert haben, der die entsprechenden Daten bereitstellt. Sie können das Argument Bedingung verwenden, um die Einschränkungskriterien direkt einzugeben. Wenn Sie beide Argumente verwenden, wendet Microsoft Office Access 2007 die WHERE-Klausel auf die Ergebnisse des Filtervorgangs an. Sie müssen mindestens eines der Argumente verwenden.

## <a name="remarks"></a>Hinweise

Sie können einen Filter oder eine Abfrage auf ein Formular in der Formularansicht oder in der Datenblattansicht anwenden.

Der angewendete Filter und die WHERE-Bedingung werden zur Einstellung der **Filter**- oder **Serverfilter**-Eigenschaft des Formulars oder des Berichts.

Für Tabellen und Formulare ist diese Aktion mit dem Klicken auf **Filter/Sortierung anwenden** oder **Serverfilter anwenden** im Menü **Datensätze** vergleichbar. Der Menübefehl wendet den zuletzt erstellten Filter auf die Tabelle oder das Formular an, wohingegen die **AnwendenFilter** -Aktion einen angegebenen Filter oder eine angegebene Abfrage anwendet.

Wenn Sie in einer Access-Datenbank im Menü Datensätze auf Filter zeigen und nach dem Ausführen der AnwendenFilter-Aktion auf Spezialfilter/-sortierung klicken, werden im Fenster Spezialfilter/-sortierung die Filterkriterien angezeigt, die Sie mit dieser Aktion ausgewählt haben.

Sie können die AnzeigenAlleDatensätze-Aktion oder den Befehl Filter/Sortierung entfernen im Menü Datensätze verwenden, um einen Filter zu entfernen und alle Datensätze einer Tabelle oder eines Formulars in einer Office Access 2007-Datenbank anzuzeigen. Wenn Sie einen Filter aus einem Access-Projekt (ADP) entfernen möchten, können Sie zum Fenster Formularbasierter Serverfilter zurückkehren, alle Filterkriterien entfernen und dann im Menü Datensätze auf der Symbolleiste auf Serverfilter anwenden klicken. Oder Sie können die FormularbasierterServerFilter-Eigenschaft auf Falsch (0) festlegen.

Beim Speichern einer Tabelle oder eines Formulars speichert Access alle Filter, die in dem Objekt derzeit definiert sind, wendet die Filter jedoch das nächste Mal, wenn das Objekt geöffnet wird, nicht an (wobei jedoch eine vor dem Speichern auf das Objekt angewendete Sortierung automatisch angewendet wird). Wenn ein Filter automatisch beim ersten Öffnen des Formulars angewendet werden soll, geben Sie ein Makro, das die **AnwendenFilter** -Aktion enthält, oder eine Ereignisprozedur mit der **ApplyFilter** -Methode des **DoCmd** -Objekts als Einstellung für die **BeimÖffnen** -Ereigniseigenschaft des Formulars an. Sie können einen Filter auch anwenden, indem Sie die **ÖffnenFormular** - oder die **ÖffnenBericht** -Aktion oder die entsprechenden Methoden verwenden. Sie können die Tabelle öffnen, indem Sie ein Makro, das die **ÖffnenTabelle** -Aktion enthält, und anschließend die **AnwendenFilter** -Aktion verwenden. Auf diese Weise wird ein Filter automatisch beim ersten Öffnen einer Tabelle angewendet.

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht die ApplyFilter-Aktion verwenden, um das Formular FrmFoods filtern, während es geöffnet wird.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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



