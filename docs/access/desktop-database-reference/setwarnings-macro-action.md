---
title: SetWarnings-Makroaktion
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710405"
---
# <a name="setwarnings-macro-action"></a>SetWarnings-Makroaktion

**Betrifft**: Access 2013, Office 2013

Verwenden Sie die **Warnmeldungen** -Aktion, um Systemmeldungen an- oder auszuschalten.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **Warnmeldungen** -Aktion hat das folgende Argument.

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
<td><p><strong>Warnmeldungen An</strong></p></td>
<td><p>Gibt an, ob Systemmeldungen angezeigt werden. Klicken Sie im Abschnitt Aktionsargumente des Bereichs Makro-Generator im Feld Warnmeldungen An auf Ja (zum Einschalten von Systemmeldungen) oder Nein (zum Ausschalten von Systemmeldungen). Die Standardeinstellung ist Nein.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Mithilfe dieser Aktion können Sie verhindern, dass gebundene Warnmeldungen und Meldungsfelder das Makro anhalten. Fehlermeldungen werden jedoch immer angezeigt. Außerdem werden von Microsoft Access nur Dialogfelder angezeigt, in denen nicht nur eine Schaltfläche ausgewählt werden muss (wie **OK**, **Abbrechen**, **Ja** oder **Nein**), sondern eine Eingabe erforderlich ist. Dazu gehören z. B. alle Dialogfelder, in denen Sie Text eingeben oder unter verschiedenen Optionen auswählen müssen.

Das Ausführen dieser Aktion mit dem Argument **Warnmeldungen An** auf **Nein** hat den gleichen Effekt wie das Drücken der EINGABETASTE in Warnmeldungen oder Meldungsfeldern. Normalerweise wird bei der Anzeige einer Warnmeldung oder eines Meldungsfelds auf eine Schaltfläche **OK** oder **Ja** geklickt.

Nach Abschluss des Makros werden die Systemmeldungen automatisch von Access wieder angeschaltet.

Diese Aktion wird häufig in Verbindung mit der **Echo** -Aktion verwendet, bei der die Ergebnisse eines Makros bis zu dessen Abschluss ausgeblendet bleiben. Mit der **Warnmeldungen** -Aktion können Sie auch die Warnmeldungen und Meldungsfelder ausblenden.

> [!WARNING]
> [!VORSICHT] Die **Warnmeldungen** -Aktion kann zwar die Interaktion mit Makros vereinfachen, das Ausschalten von Systemmeldungen sollte jedoch vorsichtig erfolgen. In einigen Fällen kann das Ausführen eines Makros unangebracht sein, wenn eine bestimmte Warnmeldung angezeigt wird. Verwenden Sie diese Aktion nur, wenn Sie sich über das Ergebnis aller Makroaktionen im Klaren sind.

Verwenden Sie die **SetWarnings** -Methode des **DoCmd** -Objekts, um die **SendenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

