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
localization_priority: Normal
ms.openlocfilehash: 8b90af8d1cda073ffa37022bb5db5e8cf8e3b978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306706"
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
<td><p>Der Name des Steuerelements, das Sie aktualisieren möchten. Geben Sie den Namen des Steuerelements in das Feld <strong>Steuerelementname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein. Sie sollten nur den Namen des Steuerelements verwenden, nicht den vollqualifizierten Bezeichner (beispielsweise <strong>Formulare</strong>!<em> Formularname</em>! <em>ControlName</em>). Lassen Sie dieses Argument leer, um die Quelle des aktiven Objekts erneut zu aktualisieren. Wenn das aktive Objekt ein Datenblatt oder ein abfrageergebnissatz ist, müssen Sie dieses Argument leer lassen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

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

Wenn Sie ein Steuerelement, das sich nicht im aktiven Objekt befindet, erneut abfragen möchten, **** müssen Sie die Requery-Methode in einem VBA-Modul (Visual Basic für Applikationen) verwenden, nicht die Requery-Aktion oder die entsprechende Requery-Methode des **DoCmd** -Objekts. **** **** Die **Requery** -Methode in VBA ist schneller **** als die Requery-Aktion oder die **DoCmd. Requery** -Methode. Darüber hinaus wird bei Verwendung der **Requery** -Aktion oder der **DoCmd. Requery** -Methode von Microsoft Access die Abfrage geschlossen und aus der Datenbank erneut geladen, aber wenn Sie die Requery-Methode verwenden, führt Access die Abfrage erneut aus, ohne Sie zu schließen und neu zu laden. **** Beachten Sie, dass die ActiveX Data Object ( **** ADO) Requery-Methode genauso funktioniert wie die Access Requery-Methode. ****

