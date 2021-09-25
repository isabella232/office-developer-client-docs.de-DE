---
title: RenameObject-Makroaktion
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: bafbde738154993f3fea0c4f2537a9807009b966
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617454"
---
# <a name="renameobject-macro-action"></a>RenameObject-Makroaktion

**Gilt für**: Access 2013, Office 2013

Zum Umbenennen eines angegebenen Datenbankobjekts können Sie die **UmbenennenObjekt** -Aktion verwenden.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist.

## <a name="setting"></a>Einstellung

Die **UmbenennenObjekt**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Neuer Name</strong></p></td>
<td><p>Ein neuer Name für das Datenbankobjekt. Geben Sie den Objektnamen in das Feld <strong>"Neuer Name"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" ein. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objekttyp</strong></p></td>
<td><p>Der Objekttyp, den Sie umbenennen möchten. Klicken Sie auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt umzubenennen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alter Name</strong></p></td>
<td><p>Der Name des Objekts, das Sie umbenennen möchten. Im Feld <strong>Alter Name</strong> werden alle Objekte in der Datenbank mit dem Typ angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt wurde. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen. 

</p><p><strong>HINWEIS:</strong>Wenn Sie ein Makro ausführen, das die <STRONG>Umbenennungsaktion</STRONG> in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Der neue Name des Datenbankobjekts muss den Standardnamenskonventionen für Access-Objekte entsprechen.

Sie können ein geöffnetes Objekt nicht umbenennen.

Wenn Sie die Argumente **Objekttyp** und **Alter Name** leer lassen, wird das im Navigationsbereich ausgewählte Objekt in Access automatisch umbenannt. Zum Auswählen eines Objekts im Navigationsbereich können Sie die **AuswählenObjekt** -Aktion mit dem Argument **Im Navigationsbereich** verwenden, das auf **Ja** festgelegt ist.

Sie können ein Objekt auch umbenennen, indem Sie im Navigationsbereich mit der rechten Maustaste darauf klicken, dann auf **Umbenennen** klicken und einen neuen Namen eingeben. Mit der **UmbenennenObjekt** -Aktion müssen Sie das Objekt nicht zuerst im Navigationsbereich auswählen und das Makro beenden, um den neuen Namen einzugeben.

Diese Aktion unterscheidet sich von der **KopierenObjekt** -Aktion, bei der eine Kopie des Objekts unter einem neuen Namen erstellt wird.

Verwenden Sie die **Rename** -Methode des **DoCmd** -Objekts, um die **UmbenennenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

