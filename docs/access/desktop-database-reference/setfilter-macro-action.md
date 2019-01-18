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
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698680"
---
# <a name="setfilter-macro-action"></a>SetFilter-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **FestlegenFilter** -Aktion wenden Sie auf die Datensätze im aktiven Datenblatt, Formular, Bericht oder in der aktuellen Tabelle einen Filter an.

## <a name="setting"></a>Einstellung

Die **FestlegenFilter** -Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p>Filter Name</p></td>
<td><p>Wenn angegeben, der Name einer Abfrage oder eines Filters, der als Abfrage gespeichert wurde. Dieses Argument oder das Argument WhereCondition ist in einer Clientdatenbank erforderlich. In einer Webdatenbank ist dieses Argument nicht verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Wenn angegeben, eine SQL-WHERE-Klausel, mit der die Datensätze im Datenblatt, Formular, Bericht oder in der Tabelle eingeschränkt werden. In einer Webdatenbank ist dieses Argument erforderlich.</p></td>
</tr>
<tr class="odd">
<td><p>Control Name</p></td>
<td><p>Wenn angegeben, der Name des Steuerelements, das dem zu filternden Unterformular oder Unterbericht entspricht. Wenn das Argument leer ist, wird das aktuelle Objekt gefiltert.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

In einer Webdatenbank darf das Bedingung-Argument nicht mit einem Gleichheitszeichen (=) beginnen.

Beim Ausführen dieser Aktion wird der Filter auf die Tabelle, das Formular, den Bericht oder das Datenblatt (z. B. Abfrageergebnis) angewendet, das aktiv ist und den Fokus besitzt.

Mit der  **Filter** -Eigenschaft des aktiven Objekts können Sie das WhereCondition-Argument speichern und zu einem späteren Zeitpunkt anwenden. Filter werden zusammen mit den Objekten gespeichert, in denen sie erstellt wurden. Sie werden zwar automatisch geladen, wenn das Objekt geöffnet wird, aber werden nicht automatisch angewendet.

Legen Sie in einer Clientdatenbank um automatisch einen Filter anwenden, wenn das Objekt geöffnet ist, die **BeimLadenFiltern** -Eigenschaft auf true fest.

Wenn Sie in einer Webdatenbank beim Öffnen eines Objekts automatisch einen Filter anwenden möchten, fügen Sie einem Makro die **FestlegenFilter** -Aktion hinzu, und fügen Sie das Makro dem **BeiLaden** -Ereignis des Objekts hinzu.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt die Verwendung der Aktion SetFilter zum Filtern des Formulars, in dem das Makro definiert wurde.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
