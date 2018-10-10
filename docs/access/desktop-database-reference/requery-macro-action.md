---
title: AktualisierenDaten-Makroaktion
TOCTitle: Requery Macro Action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9eea9445912b1a784d9926b2c044c4385a17ee69
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475079"
---
# <a name="requery-macro-action"></a>AktualisierenDaten-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Sie können die **AktualisierenDaten** -Aktion verwenden, um die Daten in einem angegebenen Steuerelement des aktiven Objekts durch erneutes Abfragen der Steuerelementquelle zu aktualisieren. Wenn kein Steuerelement angegeben ist, fragt diese Aktion die Objektquelle selbst erneut ab. Verwenden Sie diese Aktion, um sicherzustellen, dass das aktive Objekt oder eines seiner Steuerelemente die neuesten Daten anzeigt.

## <a name="setting"></a>Einstellung

Die **AktualisierenDaten** -Aktion hat das folgende Argument.

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
<td><p>Der Name des Steuerelements, das Sie aktualisieren möchten. Geben Sie den Namen des Steuerelements im Feld Steuerelementname im Abschnitt Aktionsargumente des Bereichs Makro-Generator ein. Sie sollten nur den Namen des Steuerelements, nicht den vollqualifizierten Bezeichner verwenden (wie Formulare!Formularname!Steuerelementname). Lassen Sie dieses Argument leer, um die Quelle des aktiven Objekts zu aktualisieren. Wenn das aktive Objekt ein Datenblatt oder ein Resultset einer Abfrage ist, müssen Sie dieses Argument leer lassen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die **AktualisierenDaten** -Aktion wendet eines der folgenden Verfahren an:

  - Erneutes Ausführen der Abfrage, auf der das Steuerelement oder Objekt basiert.

  - Anzeigen aller neuen oder geänderten Datensätze und Entfernen aller gelöschten Datensätze aus der Tabelle, auf der das Steuerelement bzw. Objekt basiert.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>AktualisierenDaten</STRONG> -Aktion wirkt sich nicht auf die Position des Datensatzzeigers aus.</P>



Folgende Steuerelemente können auf einer Abfrage oder Tabelle basieren:

  - Listenfelder und Kombinationsfelder.

  - Unterformularsteuerelemente.

  - OLE-Objekte, z. B. Diagramme.

  - Steuerelemente, die Domänen-Aggregatfunktionen wie **DBSUMME** enthalten.

Wenn das angegebene Steuerelement nicht auf einer Abfrage oder einer Tabelle basiert, erzwingt diese Aktion eine Neuberechnung des Steuerelements.

Wenn Sie das Argument **Steuerelementname** leer lassen, hat die **AktualisierenDaten** -Aktion dieselbe Wirkung wie das Drücken von UMSCHALTTASTE+F9, falls das Objekt den Fokus besitzt. Wenn ein Unterformularsteuerelement den Fokus hat, fragt diese Aktion nur die Quelle des Unterformulars erneut ab (wie beim Drücken von UMSCHALTTASTE+F9).


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>AktualisierenDaten</STRONG> -Aktion fragt die Herkunft des Steuerelements oder des Objekts erneut ab. Die <STRONG>AktualisierenObjekt</STRONG> -Aktion aktualisiert Steuerelemente im angegebenen Objekt, fragt jedoch die Datenbank nicht erneut ab oder zeigt keine neuen Datensätze an. Die <STRONG>AnzeigenAlleDatensätze</STRONG> -Aktion fragt nicht nur das aktive Objekt ab, sondern entfernt auch alle angewendeten Filter, was die <STRONG>AktualisierenDaten</STRONG> -Aktion nicht vornimmt.</P>



Wenn Sie ein Steuerelement erneut abfragen möchten, das sich nicht im aktiven Objekt befindet, müssen Sie die **Requery** -Methode in einem VBA-Modul (Visual Basic für Applikationen) verwenden und nicht die **AktualisierenDaten** -Aktion oder die entsprechende **Requery** -Methode des **DoCmd** -Objekts. Die **Requery** -Methode in VBA ist schneller als die **AktualisierenDaten** -Aktion oder die **DoCmd.Requery** -Methode. Wenn Sie die **AktualisierenDaten** -Aktion oder die **DoCmd.Requery** -Methode verwenden, schließt Microsoft Access außerdem die Abfrage und lädt sie aus der Datenbank neu. Wenn Sie jedoch die **Requery** -Methode verwenden, führt Access die Abfrage erneut aus, ohne sie zu schließen und neu zu laden. Beachten Sie, dass die **Requery** -Methode von ActiveX Data Objects (ADO) wie die **Requery** -Methode von Access funktioniert.

