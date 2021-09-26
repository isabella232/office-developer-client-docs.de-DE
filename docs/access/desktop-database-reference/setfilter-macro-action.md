---
title: SetFilter-Makroaktion
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d21690a0444fcae2d45596935969d63ed69fff43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611539"
---
# <a name="setfilter-macro-action"></a>SetFilter-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **FestlegenFilter**-Aktion wenden Sie auf die Datensätze im aktiven Datenblatt, Formular, Bericht oder in der aktuellen Tabelle einen Filter an.

## <a name="setting"></a>Einstellung

Die **FestlegenFilter**-Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p>Der Name einer Abfrage oder eines Filters, der als Abfrage gespeichert wurde (sofern angegeben). In Clientdatenbanken ist dieses Argument oder das Argument WhereCondition erforderlich. In einer Webdatenbank ist dieses Argument nicht verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Eine SQL WHERE-Klausel, die die Datensätze im Datenblatt, im Formular, im Bericht oder in der Tabelle einschränkt (sofern angegeben). In einer Webdatenbank ist dieses Argument erforderlich.</p></td>
</tr>
<tr class="odd">
<td><p>Steuerelementname</p></td>
<td><p>Der Name des Steuerelements, das dem zu filternden Unterformular oder Unterbericht entspricht (sofern angegeben). Ohne Angabe wird das aktuelle Objekt gefiltert.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

In einer Webdatenbank darf das Argument Where Condition nicht mit einem Gleichheitszeichen (=) beginnen.

Beim Ausführen dieser Aktion wird der Filter auf die Tabelle, das Formular, den Bericht oder das Datenblatt (z. B. Abfrageergebnis) angewendet, das aktiv ist und den Fokus besitzt.

Mit der  **Filter** -Eigenschaft des aktiven Objekts können Sie das WhereCondition-Argument speichern und zu einem späteren Zeitpunkt anwenden. Filter werden zusammen mit den Objekten gespeichert, in denen sie erstellt wurden. Sie werden zwar automatisch geladen, wenn das Objekt geöffnet wird, aber werden nicht automatisch angewendet.

Um in einer Clientdatenbank automatisch einen Filter anzuwenden, wenn das Objekt geöffnet wird, legen Sie die **FilterOnLoad-Eigenschaft** auf "True" fest.

Wenn Sie in einer Webdatenbank beim Öffnen eines Objekts automatisch einen Filter anwenden möchten, fügen Sie einem Makro die **FestlegenFilter**-Aktion hinzu, und fügen Sie das Makro dem **BeiLaden**-Ereignis des Objekts hinzu.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt die Verwendung der Aktion SetFilter zum Filtern des Formulars, in dem das Makro definiert wurde.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
