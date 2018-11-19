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
ms.openlocfilehash: 253067d61a496073692ea4e462b9b0a67f0e26cd
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026295"
---
# <a name="saveobject-macro-action"></a>SaveObject-Makroaktion

**Betrifft**: Access 2013, Office 2013

Die **Speichernobjekt** -Aktion können Sie eine angegebene Access-Objekt oder das aktive Objekt speichern, wenn keines angegeben ist. Sie können auch das aktive Objekt unter einem neuen Namen in einigen Fällen speichern (diese Funktion identisch mit dem Befehl **Speichern unter** auf der **Symbolleiste für den Schnellzugriff**).

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **SpeichernObjekt** -Aktion hat die folgenden Argumente.

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
<td><p>Der zu speichernde Objekttyp. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Um das aktive Objekt auszuwählen, lassen Sie dieses Argument leer. Wenn Sie in diesem Argument einen Objekttyp auswählen, müssen Sie einen Namen eines bereits vorhandenen Objekts im Argument Objektname auswählen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des Objekts gespeichert werden soll. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank mit dem Objekttyp angezeigt, der mit dem <strong>Objekttyp</strong> -Argument ausgewählt wurde. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, können Sie lassen dieses Argument leer, um das aktive Objekt speichern oder, in einigen Fällen geben Sie einen neuen Namen in dieses Argument auf das aktive Objekt mit diesem Namen zu speichern. Wenn Sie einen neuen Namen eingeben, muss der Name den Standardnamenskonventionen für Microsoft Access-Objekte entsprechen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die **Speichernobjekt** -Aktion funktioniert für alle Datenbankobjekte, die der Benutzer explizit öffnen kann, und speichern. Das angegebene Objekt muss für die **Speichernobjekt** -Aktion haben keinen Einfluss auf das Objekt geöffnet sein. Diese Aktion hat dieselbe Wirkung wie das Auswählen eines Objekts und klicken Sie dann speichern, indem Sie auf der **Symbolleiste für den Schnellzugriff**auf **Speichern** . 

Das Argument **Objekttyp** leer lassen und einen neuen Namen eingeben, in das Argument **Objektname** hat dieselbe Wirkung wie das **Speichern unter** auf der **Symbolleiste für den Schnellzugriff**klicken und eingeben einen neuen Namen für das aktive Objekt. Verwenden die **Speichernobjekt** -Aktion können Sie ein Objekt angeben, speichern und den Befehl **Speichern unter** aus einem Makro ausführen.

> [!NOTE]
> [!HINWEIS] Zum Speichern der folgenden Objekte unter einem neuen Namen können Sie die **SpeichernObjekt** -Aktion nicht verwenden:
> - Ein Formular in der Formularansicht oder Datenblattansicht
> - Einen Bericht in der Seitenansicht
> - Ein Modul
> - Eine Serversicht in der Datenblattansicht oder Seitenansicht
> - Eine Datenzugriffsseite in der Seitenansicht
> - Eine Tabelle in der Datenblattansicht oder Seitenansicht
> - Eine Abfrage in der Datenblattansicht oder Seitenansicht
> - Eine gespeicherte Prozedur in der Datenblattansicht oder Seitenansicht

Die **SpeichernObjekt** -Aktion, unabhängig davon, ob in einem in der aktuellen Datenbank ausgeführten Makro oder in einer Bibliotheksdatenbank ausgeführt, speichert immer das angegebene Objekt oder das aktive Objekt in der Datenbank, in der das Objekt erstellt wurde.

Wenn Sie das aktive Objekt unter einem neuen Namen speichern, der Name jedoch mit dem Namen eines bereits vorhandenen Objekts übereinstimmt, werden Sie in einem Dialogfeld gefragt, ob Sie das vorhandene Objekt überschreiben möchten. Wenn Sie das Argument **Warnungen** der **Warnmeldungen** -Aktion auf **Nein** festgelegt haben, wird das Dialogfeld nicht angezeigt, und das alte Objekt wird automatisch überschrieben.

Verwenden Sie die **Save** -Methode des **DoCmd** -Objekts, um die **SpeichernObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

