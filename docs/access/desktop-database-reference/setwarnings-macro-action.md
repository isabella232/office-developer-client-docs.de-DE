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
ms.localizationpriority: medium
ms.openlocfilehash: 0e25214d4ca7e6779efa127da71f63edef429e23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585319"
---
# <a name="setwarnings-macro-action"></a>SetWarnings-Makroaktion

**Gilt für**: Access 2013, Office 2013

Verwenden Sie die **Warnmeldungen** -Aktion, um Systemmeldungen an- oder auszuschalten.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **Warnmeldungen**-Aktion hat das folgende Argument.

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
<td><p>Gibt an, ob Systemmeldungen angezeigt werden. Klicken Sie im Feld <strong>"Warnungen</strong> an" im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" auf <strong>"Ja"</strong> (um Systemmeldungen zu aktivieren) oder auf <strong>"Nein"</strong> (um Systemmeldungen zu deaktivieren). Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe dieser Aktion können Sie verhindern, dass gebundene Warnmeldungen und Meldungsfelder das Makro anhalten. Fehlermeldungen werden jedoch immer angezeigt. Außerdem werden von Microsoft Access nur Dialogfelder angezeigt, in denen nicht nur eine Schaltfläche ausgewählt werden muss (wie **OK**, **Abbrechen**, **Ja** oder **Nein**), sondern eine Eingabe erforderlich ist. Dazu gehören z. B. alle Dialogfelder, in denen Sie Text eingeben oder unter verschiedenen Optionen auswählen müssen.

Das Ausführen dieser Aktion mit dem Argument **Warnmeldungen An** auf **Nein** hat den gleichen Effekt wie das Drücken der EINGABETASTE in Warnmeldungen oder Meldungsfeldern. Normalerweise wird bei der Anzeige einer Warnmeldung oder eines Meldungsfelds auf eine Schaltfläche **OK** oder **Ja** geklickt.

Nach Abschluss des Makros werden die Systemmeldungen automatisch von Access wieder angeschaltet.

Diese Aktion wird häufig in Verbindung mit der **Echo** -Aktion verwendet, bei der die Ergebnisse eines Makros bis zu dessen Abschluss ausgeblendet bleiben. Mit der **Warnmeldungen** -Aktion können Sie auch die Warnmeldungen und Meldungsfelder ausblenden.

> [!WARNING]
> [!VORSICHT] Die **Warnmeldungen** -Aktion kann zwar die Interaktion mit Makros vereinfachen, das Ausschalten von Systemmeldungen sollte jedoch vorsichtig erfolgen. In einigen Fällen kann das Ausführen eines Makros unangebracht sein, wenn eine bestimmte Warnmeldung angezeigt wird. Verwenden Sie diese Aktion nur, wenn Sie sich über das Ergebnis aller Makroaktionen im Klaren sind.

Verwenden Sie die **SetWarnings** -Methode des **DoCmd** -Objekts, um die **SendenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

