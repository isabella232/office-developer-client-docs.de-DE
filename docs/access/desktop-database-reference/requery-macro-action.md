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
ms.openlocfilehash: a0f951c69939e8265bab64193e594eed32149c38
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920032"
---
# <a name="requery-macro-action"></a>Requery-Makroaktion


**Betrifft**: Access 2013, Office 2013

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



Wenn Sie ein Steuerelement erneut abfragen, die für das aktive Objekt ist nicht möchten, müssen Sie die **Requery** -Methode in einem Visual Basic für Applikationen (VBA) Modul, nicht die **AktualisierenDaten** -Aktion oder die entsprechende **Requery** -Methode des **DoCmd** -Objekts verwenden. Die **Requery** -Methode in VBA ist schneller als die **AktualisierenDaten** -Aktion oder die **Requery** -Methode. Darüber hinaus wird, wenn Sie die **AktualisierenDaten** -Aktion oder die **Requery** -Methode verwenden, schließt Microsoft Access die Abfrage und lädt ihn erneut aus der Datenbank, aber bei Verwendung die **Requery** -Methode führt Access ohne Schließen und neu zu laden. Beachten Sie, dass das ActiveX-Objekt (ADO) **Requery** -Methode die gleiche Weise wie die Access **Requery** -Methode funktioniert.

