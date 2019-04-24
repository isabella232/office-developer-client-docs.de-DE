---
title: SaveObject-Makroaktion
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308932"
---
# <a name="saveobject-macro-action"></a>SaveObject-Makroaktion

**Gilt für**: Access 2013, Office 2013

You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **SpeichernObjekt**-Aktion hat die folgenden Argumente.

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
<td><p>Der Objekttyp, der gespeichert werden soll. Klicken Sie im Feld <strong>Objekttyp</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen. Wenn Sie einen Objekttyp in diesem Argument auswählen, müssen Sie den Namen eines vorhandenen Objekts im Argument <strong>Objektname</strong> auswählen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des zu speichernden Objekts. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt ist. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, können Sie dieses Argument leer lassen, um das aktive Objekt zu speichern, oder in einigen Fällen einen neuen Namen in dieses Argument eingeben, um das aktive Objekt mit diesem Namen zu speichern. Wenn Sie einen neuen Namen eingeben, muss der Name den Standardnamenskonventionen für Microsoft Access-Objekte entsprechen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

The **SaveObject** action works on all database objects that the user can explicitly open and save. The specified object must be open for the **SaveObject** action to have any effect on the object. This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**. 

Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object. Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.

> [!NOTE]
> [!HINWEIS] Zum Speichern der folgenden Objekte unter einem neuen Namen können Sie die **SpeichernObjekt** -Aktion nicht verwenden:
> - Ein Formular in der Formularansicht oder Datenblattansicht
> - Ein Bericht in der Seitenansicht
> - Ein Modul
> - Eine Serveransicht in der Datenblattansicht oder-Vorschau
> - Eine Datenzugriffsseite in der Seitenansicht
> - Eine Tabelle in der Datenblattansicht oder der Seitenansicht
> - Eine Abfrage in der Datenblattansicht oder der Seitenansicht
> - Eine gespeicherte Prozedur in der Datenblattansicht oder der Seitenansicht

Die **SpeichernObjekt** -Aktion, unabhängig davon, ob in einem in der aktuellen Datenbank ausgeführten Makro oder in einer Bibliotheksdatenbank ausgeführt, speichert immer das angegebene Objekt oder das aktive Objekt in der Datenbank, in der das Objekt erstellt wurde.

Wenn Sie das aktive Objekt unter einem neuen Namen speichern, der Name jedoch mit dem Namen eines bereits vorhandenen Objekts übereinstimmt, werden Sie in einem Dialogfeld gefragt, ob Sie das vorhandene Objekt überschreiben möchten. Wenn Sie das Argument **Warnungen** der **Warnmeldungen** -Aktion auf **Nein** festgelegt haben, wird das Dialogfeld nicht angezeigt, und das alte Objekt wird automatisch überschrieben.

Verwenden Sie die **Save** -Methode des **DoCmd** -Objekts, um die **SpeichernObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

