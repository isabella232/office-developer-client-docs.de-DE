---
title: SelectObject-Makroaktion
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308729"
---
# <a name="selectobject-macro-action"></a>SelectObject-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **AuswählenObjekt**-Aktion zur Auswahl eines bestimmten Datenbankobjekts verwenden.

## <a name="setting"></a>Einstellung

Die **AuswählenObjekt**-Aktion hat die folgenden Argumente.

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
<td><p>Der Typ des auszuwählenden Datenbankobjekts. Klicken Sie im Feld <strong>Objekttyp</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des auszuwählenden Objekts. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt ist. Dies ist ein erforderliches Argument, es sei denn, Sie legen das Argument im Navigationsbereich auf <strong>Ja</strong>fest.</p><p><strong>Hinweis</strong>: die Objektnamen für <STRONG>Server Ansicht</STRONG>-, <STRONG>Diagramm</STRONG>-oder <STRONG>gespeicherte Prozedur</STRONG> Objekte werden nicht im Feld <STRONG>Objekt Name</STRONG> eines Access-Projekts (ADP) angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Im Navigationsbereich</strong></p></td>
<td><p>Gibt an, ob Microsoft Access das Objekt im Navigationsbereich auswählt. Klicken Sie auf <strong>Ja</strong> (um das Objekt im Navigationsbereich auszuwählen) oder <strong>Nein</strong> (um das Objekt nicht im Navigationsbereich auszuwählen). Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **AuswählenObjekt**-Aktion funktioniert mit allen Access-Objekten, die den Fokus erhalten können. Diese Aktion weist den Fokus dem angegebenen Objekt zu und zeigt dem Objekt an, ob es ausgeblendet ist. Wenn das Objekt ein Formular ist, wird die **Sichtbar**-Eigenschaft des Formulars von der **AuswählenObjekt**-Aktion auf **Ja** festgelegt, und das Formular wird in den Modus zurückgesetzt, der durch die Formulareigenschaften festgelegt ist (beispielsweise gebundenes Formular oder Popupformular).

Wenn das Objekt in einem der anderen Access-Fenster nicht geöffnet ist, können Sie es auswählen, indem Sie das Argument **Im Navigationsbereich** auf **Ja** festlegen. Wenn Sie das Argument **Im Navigationsbereich** auf **Nein** festlegen, wird eine Fehlermeldung angezeigt, sobald Sie versuchen, ein Objekt auszuwählen, das nicht geöffnet ist.

Diese Aktion verwenden Sie unter Umständen häufig, um ein Objekt auszuwählen, für das Sie weitere Aktionen durchführen möchten. Wenn Access z. B. für die Verwendung von überlappenden Fenstern anstatt von Dokumenten mit Registerkarten konfiguriert ist, können Sie beispielsweise ein Objekt wiederherstellen, das minimiert wurde (indem Sie die **WiederherstellenFenster** -Aktion verwenden), oder ein Fenster maximieren, das ein Objekt enthält, mit dem Sie arbeiten möchten (indem Sie die **MaximierenFenster** -Aktion verwenden).

Wenn Sie ein Formular auswählen, können Sie die Aktionen **GeheZuSteuerelement**, **GeheZuDatensatz** und **GeheZuSeite** verwenden, um zu verschiedenen Formularbereichen zu wechseln. Die **GeheZuDatensatz** -Aktion funktioniert außerdem für Datenblätter.

Verwenden Sie die **SelectObject** -Methode des **DoCmd** -Objekts, um die **AuswählenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

