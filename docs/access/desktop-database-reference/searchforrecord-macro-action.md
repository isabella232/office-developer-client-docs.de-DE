---
title: SuchenNachDatensatz-Makroaktion
TOCTitle: SearchForRecord Macro Action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 21efa96338363646be826248e6c9ca0b951496c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473056"
---
# <a name="searchforrecord-macro-action"></a>SuchenNachDatensatz-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Sie können die **SuchenNachDatensatz** -Aktion verwenden, um nach einem bestimmten Datensatz in einer Tabelle, einer Abfrage, einem Formular oder einem Bericht zu suchen.

## <a name="setting"></a>Einstellung

Die **SuchenNachDatensatz** -Aktion verwendet die folgenden Argumente.

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
<td><p>Geben Sie den Datenbankobjekttyp ein, in dem Sie suchen, oder wählen Sie ihn aus. Sie können <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong> oder <strong>Bericht</strong> auswählen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Geben Sie das Objekt ein, das den zu suchenden Datensatz enthält, oder wählen Sie es aus. In der Dropdownliste werden alle Datenbankobjekte angezeigt, die den durch das Argument <strong>Objekttyp</strong> ausgewählten Typ aufweisen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Geben Sie den Ausgangspunkt und die Richtung für die Suche an.</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Einstellung</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Vorherige</strong></p></td>
<td><p>Sucht vom aktuellen Datensatz ausgehend rückwärts.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nächste</strong></p></td>
<td><p>Sucht vom aktuellen Datensatz ausgehend vorwärts.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Erster</strong></p></td>
<td><p>Sucht vom ersten Datensatz ausgehend vorwärts. Das ist der Standardwert für dieses Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Letzter</strong></p></td>
<td><p>Sucht vom letzten Datensatz ausgehend rückwärts.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Geben Sie die Kriterien für die Suche mit derselben Syntax wie eine SQL WHERE-Klausel ohne das Wort nur &quot;, in dem&quot;. Beispiel:</p>
<p>`Description = "Beverages"`</p>
<p>Um ein Kriterium erstellen, die einen Wert aus einem Textfeld auf einem Formular enthält, müssen Sie einen Ausdruck erstellen, der mit dem Namen des Textfelds mit dem Wert für die Suche den ersten Teil der Kriterien verkettet. Das folgende Kriterium wird beispielsweise das Feld Beschreibung für den Wert in das Textfeld mit dem Namen auf dem Formular mit dem Namen FrmCategories TxtDescription gesucht. Ein Gleichheitszeichen (<strong>=</strong>) am Anfang des Ausdrucks und die Verwendung von Hochkommas (<strong>'</strong>) auf beiden Seiten des Verweises im Feld Text:</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

- Falls mehrere Datensätze mit den Kriterien im Argument **Bedingung** übereinstimmen, legen die folgenden Einstellungen fest, welcher Datensatz gefunden wird:
    
  - **Der Datensatz argumenteinstellung** Finden Sie in der Tabelle im Abschnitt Einstellungen für Weitere Informationen zum Argument **Datensatz** .
    
  - **Die Sortierreihenfolge der Datensätze** Angenommen, wenn das Argument **Datensatz** auf der **ersten**festgelegt ist, kann die Sortierreihenfolge der Datensätze ändern welcher Datensatz gefunden wird.

- Das im Argument **Objektname** angegebene Argument muss vor dem Ausführen dieser Aktion geöffnet werden. Sonst treten Fehler auf.

- Werden die Kriterien im Argument **Bedingung** nicht gefunden, tritt kein Fehler auf, und der Fokus verbleibt auf dem aktuellen Datensatz.

- Bei der Suche nach dem vorherigen oder nächsten Datensatz findet kein "Umbruch" statt, wenn das Ende der Daten erreicht wird. Sind keine weiteren Datensätze vorhanden, die den Kriterien entsprechen, tritt kein Fehler auf, und der Fokus verbleibt auf dem aktuellen Datensatz. Wenn Sie bestätigen möchten, dass eine Übereinstimmung gefunden wurde, können Sie eine Bedingung für die nächste Aktion eingeben und festlegen, dass die Bedingung den im Argument **Bedingung** angegebenen Kriterien entspricht.

- Verwenden Sie die **SuchenNachDatensatz** -Methode des **DoCmd** -Objekts, um die **SuchenNachDatensatz** -Aktion in einem VBA-Modul auszuführen.

- Die **SuchenNachDatensatz** -Aktion ähnelt der **[SuchenDatensatz](findrecord-macro-action.md)** -Aktion, allerdings verfügt **SuchenNachDatensatz** über leistungsfähigere Suchfunktionen. Die **SuchenDatensatz** -Aktion wird hauptsächlich für die Suche nach Zeichenfolgen verwendet und dupliziert die Funktionen des Dialogfelds **Suchen**. Die Kriterien der **SuchenNachDatensatz** -Aktion entsprechen dagegen eher einem Filter oder einer SQL-Abfrage. Die folgende Liste bietet Verwendungsbeispiele für die **SuchenNachDatensatz** -Aktion:
    
  - Sie können komplexe Kriterien im Argument **Bedingung** verwenden, z. B.
        
    `Description = "Beverages" and CategoryID = 11`
    
  - Sie können auf Felder verweisen, die zwar in der Datensatzquelle eines Formulars oder Berichts angezeigt werden, nicht aber im Formular oder Bericht. Im vorstehenden Beispiel muss Beschreibung weder CategoryID auf das Formular oder der Bericht für die Kriterien funktionieren angezeigt werden.
    
  - Sie können logische Operatoren verwenden, z. B. **\<**, **\>**, **AND**, **OR** und **BETWEEN**. Mit der **SuchenDatensatz** -Aktion werden nur Zeichenfolgen gefunden, die der gesuchten Zeichenfolge entsprechen, mit dieser beginnen oder sie enthalten.

## <a name="example"></a>Beispiel

Mit dem folgenden Makro wird durch Verwendung der ÖffnenTabelle-Aktion zuerst die Tabelle Kategorien geöffnet. Anschließend sucht das Makro mithilfe der SuchenNachDatensatz-Aktion nach dem ersten Datensatz in der Tabelle, dessen Feld Description dem Wert "Getränke" entspricht.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktion</p></th>
<th><p>Argumente</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>OpenTable</strong></p></td>
<td><p><strong>Tabellenname</strong>: Kategorien<strong>Anzeigen</strong>: <strong>DatasheetData Modus</strong>: <strong>Bearbeiten</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>SearchForRecord</strong></p></td>
<td><p><strong>Objekttyp</strong>: <strong>TableObject Name</strong>: Kategorien<strong>Record</strong>: <strong>FirstWhere Bedingung</strong>: Description = &quot;Getränke&quot;</p></td>
</tr>
</tbody>
</table>

