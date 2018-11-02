---
title: RepaintObject-Makroaktion
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 369c518ab0ab213975bb7da3c96b6e5844bad9ee
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919416"
---
# <a name="repaintobject-macro-action"></a>RepaintObject-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **AktualisierenObjekt** -Aktion verwenden, um alle ausstehenden Bildschirmaktualisierungen für ein angegebenes Datenbankobjekt oder für das aktive Datenbankobjekt durchzuführen, falls keines angegeben ist. Zu solchen Aktualisierungen gehören alle ausstehenden Neuberechnungen für die Steuerelemente des Objekts.

## <a name="setting"></a>Einstellung

Die **AktualisierenObjekt** -Aktion verwendet die folgenden Argumente.

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
<td><p>Der Typ des zu aktualisierenden Objekts. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des zu aktualisierenden Objekts. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt ist. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Microsoft Access wartet mit dem Beenden ausstehender Bildschirmaktualisierungen, bis andere ausstehende Aufgaben beendet sind. Mit dieser Aktion können Sie die sofortige Aktualisierung der Steuerelemente im angegebenen Objekt erzwingen. In den folgenden Fällen können Sie diese Aktion verwenden:

  - Wenn Sie die **SetzenWert** -Aktion zum Ändern von Werten für eine Vielzahl von Steuerelementen verwenden. In Access werden die Änderungen möglicherweise nicht unmittelbar angezeigt, insbesondere, wenn andere Steuerelemente (wie berechnete Steuerelemente) von Werten des geänderten Steuerelements abhängen.

  - Wenn Sie sicher gehen möchten, dass das angezeigte Formular Daten in all seinen Steuerelementen anzeigt. Beispielsweise zeigen Steuerelemente, die OLE-Objekte enthalten, ihre Daten nicht unmittelbar nach Öffnen eines Formulars an.


> [!NOTE]
> <UL>
> <LI>
> <P>Diese Aktion verursacht keine erneute Abfrage der Datenbank, sodass keine neuen und geänderten Datensätze angezeigt oder Datensätze aus der zugrunde liegenden Tabelle oder der zugrunde liegenden Abfrage des Objekts entfernt werden. Verwenden Sie zur erneuten Abfrage der Objektquelle oder eines ihrer Steuerelemente die <STRONG>AktualisierenDaten</STRONG> -Aktion. Verwenden Sie die <STRONG>AnzeigenAlleDatensätze</STRONG> -Aktion, um die neuesten Datensätze anzuzeigen, und entfernen Sie eventuell angewendete Filter.</P>
> <LI>
> <P>Die <STRONG>AktualisierenObjekt</STRONG> -Aktion hat dieselbe Wirkung wie das Klicken auf <STRONG>Aktualisieren</STRONG> in der Gruppe <STRONG>Datensätze</STRONG>auf der Registerkarte <STRONG>Start</STRONG>, durch das alle Änderungen angezeigt werden, die Sie oder andere Benutzer an den aktuell angezeigten Datensätzen in Formularen und Datenblättern vorgenommen haben.</P></LI></UL>



Verwenden Sie die **RepaintObject** -Methode des **DoCmd** -Objekts, um die **AktualisierenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

