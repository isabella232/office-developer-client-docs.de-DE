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
ms.openlocfilehash: f134a43aaa56a1b206330175658f92e5076a4a14
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919290"
---
# <a name="selectobject-macro-action"></a>SelectObject-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **AuswählenObjekt** -Aktion zur Auswahl eines bestimmten Datenbankobjekts verwenden.

## <a name="setting"></a>Einstellung

Die **AuswählenObjekt** -Aktion hat die folgenden Argumente.

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
<td><p>Der Name des auszuwählenden Objekts. Im Feld Objektname werden alle Objekte in der Datenbank angezeigt, die dem vom Argument Objekttyp ausgewählten Typ entsprechen. Das ist ein erforderliches Argument, es sei denn, Sie legen das Argument Im Navigationsbereich auf Ja fest.</p>

> [!NOTE]
> <P>Die Objektnamen für <STRONG>Serversicht</STRONG>, <STRONG>Diagramm</STRONG> oder <STRONG>Gespeicherte Prozedur</STRONG>-Objekte werden im Feld <STRONG>Objektname</STRONG> eines Access-Projekts (ADP) nicht angezeigt.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>Im Navigationsbereich</strong></p></td>
<td><p>Gibt an, ob Microsoft Access das Objekt im Navigationsbereich auswählt. Klicken Sie auf <strong>Ja</strong> (um das Objekt im Navigationsbereich auszuwählen) oder <strong>Nein</strong> (um das Objekt nicht im Navigationsbereich auszuwählen). Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die **AuswählenObjekt** -Aktion funktioniert mit allen Access-Objekten, die den Fokus erhalten können. Diese Aktion weist den Fokus dem angegebenen Objekt zu und zeigt dem Objekt an, ob es ausgeblendet ist. Wenn das Objekt ein Formular ist, wird die **Sichtbar** -Eigenschaft des Formulars von der **AuswählenObjekt** -Aktion auf **Ja** festgelegt, und das Formular wird in den Modus zurückgesetzt, der durch die Formulareigenschaften festgelegt ist (beispielsweise gebundenes Formular oder Popupformular).

Wenn das Objekt in einem der anderen Access-Fenster nicht geöffnet ist, können Sie es auswählen, indem Sie das Argument **Im Navigationsbereich** auf **Ja** festlegen. Wenn Sie das Argument **Im Navigationsbereich** auf **Nein** festlegen, wird eine Fehlermeldung angezeigt, sobald Sie versuchen, ein Objekt auszuwählen, das nicht geöffnet ist.

Diese Aktion verwenden Sie unter Umständen häufig, um ein Objekt auszuwählen, für das Sie weitere Aktionen durchführen möchten. Wenn Access z. B. für die Verwendung von überlappenden Fenstern anstatt von Dokumenten mit Registerkarten konfiguriert ist, können Sie beispielsweise ein Objekt wiederherstellen, das minimiert wurde (indem Sie die **WiederherstellenFenster** -Aktion verwenden), oder ein Fenster maximieren, das ein Objekt enthält, mit dem Sie arbeiten möchten (indem Sie die **MaximierenFenster** -Aktion verwenden).

Wenn Sie ein Formular auswählen, können Sie die Aktionen **GeheZuSteuerelement**, **GeheZuDatensatz** und **GeheZuSeite** verwenden, um zu verschiedenen Formularbereichen zu wechseln. Die **GeheZuDatensatz** -Aktion funktioniert außerdem für Datenblätter.

Verwenden Sie die **SelectObject** -Methode des **DoCmd** -Objekts, um die **AuswählenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

