---
title: DeleteObject-Makroaktion
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3ed8580d95128dae475a6d5fe3963f7daaad53f0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997259"
---
# <a name="deleteobject-macro-action"></a>DeleteObject-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können die **LöschenObjekt** -Aktion verwenden, um ein angegebenes Datenbankobjekt zu löschen.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **LöschenObjekt** -Aktion hat die folgenden Argumente.

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
<td><p>Der Typ des Objekts, das gelöscht werden soll. Klicken Sie im Feld Objekttyp im Bereich Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt zu löschen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des zu löschenden Objekts. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank mit dem Objekttyp angezeigt, der mit dem <strong>Objekttyp</strong> -Argument ausgewählt wurde. Lassen Sie dieses Feld leer, wenn Sie im Feld <strong>Objekttyp</strong> leer lassen. Wenn Sie ein Makro ausführen, das die <strong>LöschenObjekt</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Office Access 2007 zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> [!VORSICHT] Wenn Sie die Felder **Objekttyp** und **Objektname** leer lassen, löscht Access beim Auftreten der **LöschenObjekt** -Aktion das im Navigationsbereich ausgewählte Objekt, ohne eine Warnmeldung anzuzeigen.

## <a name="remarks"></a>Hinweise

Sie können die **LöschenObjekt** -Aktion verwenden, um temporäre Objekte zu löschen, die beim Ausführen des Makros erstellt wurden. Beispielsweise können Sie die **ÖffnenAbfrage** -Aktion verwenden, um eine Tabellenerstellungsabfrage zum Erstellen einer temporären Tabelle auszuführen. Wenn die temporäre Tabelle nicht mehr verwendet wird, können Sie sie mithilfe der **LöschenObjekt** -Aktion löschen.

Diese Aktion wirkt sich genauso aus, wie wenn Sie ein Objekt im Navigationsbereich auswählen und anschließend die ENTF-TASTE drücken, oder wenn Sie mit der rechten Maustaste auf das Objekt im Navigationsbereich klicken und dann auf **Löschen** klicken.

Verwenden Sie die **DeleteObject** -Methode des **DoCmd** -Objekts, um die **LöschenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

