---
title: Requery-Makroaktion
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3ff41c7a1d22f58a8a462b82dcd080e442a7254e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611595"
---
# <a name="requery-macro-action"></a>Requery-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **AktualisierenDaten** -Aktion verwenden, um die Daten in einem angegebenen Steuerelement des aktiven Objekts durch erneutes Abfragen der Steuerelementquelle zu aktualisieren. Wenn kein Steuerelement angegeben ist, fragt diese Aktion die Objektquelle selbst erneut ab. Verwenden Sie diese Aktion, um sicherzustellen, dass das aktive Objekt oder eines seiner Steuerelemente die neuesten Daten anzeigt.

## <a name="setting"></a>Einstellung

Die **AktualisierenDaten**-Aktion hat das folgende Argument.

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
<td><p><strong>Steuerelementname</strong></p></td>
<td><p>Der Name des Steuerelements, das Sie aktualisieren möchten. Geben Sie den Namen des Steuerelements in das Feld <strong>"Steuerelementname"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" ein. Sie sollten nur den Namen des Steuerelements und nicht den vollqualifizierten Bezeichner (z. B. <strong>Forms</strong>!<em> Formname</em>! <em>controlname</em>). Lassen Sie dieses Argument leer, um die Quelle des aktiven Objekts erneut abzuabfragen. Wenn das aktive Objekt ein Datenblatt oder ein Abfrageergebnissatz ist, müssen Sie dieses Argument leer lassen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Die **AktualisierenDaten**-Aktion wendet eines der folgenden Verfahren an:

- Erneutes Ausführen der Abfrage, auf der das Steuerelement oder Objekt basiert.

- Anzeigen aller neuen oder geänderten Datensätze und Entfernen aller gelöschten Datensätze aus der Tabelle, auf der das Steuerelement bzw. Objekt basiert.

> [!NOTE]
> [!HINWEIS] Die **AktualisierenDaten** -Aktion wirkt sich nicht auf die Position des Datensatzzeigers aus.

Folgende Steuerelemente können auf einer Abfrage oder Tabelle basieren:

- Listenfelder und Kombinationsfelder.

- Unterformularsteuerelemente.

- OLE-Objekte, z. B. Diagramme.

- Steuerelemente, die Domänen-Aggregatfunktionen wie **DBSUMME** enthalten.

Wenn das angegebene Steuerelement nicht auf einer Abfrage oder einer Tabelle basiert, erzwingt diese Aktion eine Neuberechnung des Steuerelements.

Wenn Sie das Argument **Steuerelementname** leer lassen, hat die **AktualisierenDaten** -Aktion dieselbe Wirkung wie das Drücken von UMSCHALTTASTE+F9, falls das Objekt den Fokus besitzt. Wenn ein Unterformularsteuerelement den Fokus hat, fragt diese Aktion nur die Quelle des Unterformulars erneut ab (wie beim Drücken von UMSCHALTTASTE+F9).

> [!NOTE]
> [!HINWEIS] Die **AktualisierenDaten** -Aktion fragt die Herkunft des Steuerelements oder des Objekts erneut ab. Die **AktualisierenObjekt** -Aktion aktualisiert Steuerelemente im angegebenen Objekt, fragt jedoch die Datenbank nicht erneut ab oder zeigt keine neuen Datensätze an. Die **AnzeigenAlleDatensätze** -Aktion fragt nicht nur das aktive Objekt ab, sondern entfernt auch alle angewendeten Filter, was die **AktualisierenDaten** -Aktion nicht vornimmt.

Wenn Sie ein Steuerelement erneut abfragen möchten, das sich nicht im aktiven Objekt befindet, müssen Sie die **Requery-Methode** in einem Visual Basic for Applications(VBA)-Modul verwenden, nicht in der **Requery-Aktion** oder der entsprechenden **Requery-Methode** des **DoCmd-Objekts.** Die **Requery-Methode** in VBA ist schneller als die **Requery-Aktion** oder die **DoCmd.Requery-Methode.** Wenn Sie außerdem die **Requery-Aktion** oder die **DoCmd.Requery-Methode** verwenden, schließt Microsoft Access die Abfrage und lädt sie erneut aus der Datenbank. Wenn Sie jedoch die **Requery-Methode** verwenden, wird die Abfrage von Access erneut ausgeführt, ohne sie zu schließen und erneut zu laden. Beachten Sie, dass die **Requery-Methode** ActiveX Data-Objekt (ADO) auf die gleiche Weise funktioniert wie die Access **Requery-Methode.**

