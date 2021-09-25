---
title: CloseWindow-Makroaktion
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 25d4f49d9a7afd7cbbd915c80895a3de789ac161
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577577"
---
# <a name="closewindow-macro-action"></a>CloseWindow-Makroaktion


**Gilt für**: Access 2013, Office 2013

Sie können die **CloseWindow-Aktion** verwenden, um entweder eine angegebene Access-Dokumentregisterkarte oder die aktive Dokumentregisterkarte zu schließen, wenn keine angegeben ist.

## <a name="setting"></a>Einstellung

Die **FensterSchließen**-Aktion hat die folgenden Argumente.

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
<td><p>Der Objekttyp, dessen Dokumentregisterkarte geschlossen werden soll. Klicken Sie im Feld <strong>Objekttyp</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Um die aktive Dokumentregisterkarte auszuwählen, lassen Sie dieses Argument leer.</p>

> [!NOTE]
> Wenn Sie ein Modul im Visual Basic-Editor schließen, müssen Sie **Modul** im Argument **Objekttyp** verwenden.


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname</strong></p></td>
<td><p>Der Name des Objekts, das geschlossen werden soll. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der mit dem Argument <strong>Objekttyp</strong> ausgewählt wird. Klicken Sie auf das zu schließende Objekt. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Gibt an, ob beim Schließen des Objekts Änderungen am Objekt gespeichert werden sollen. Klicken Sie auf <strong>Ja</strong> (Objekt speichern), auf <strong>Nein</strong> (Objekt schließen, ohne es zu speichern) oder auf <strong>Eingabeaufforderung</strong> (der Benutzer wird gefragt, ob das Objekt gespeichert werden soll). Die Standardeinstellung ist <strong>Eingabeaufforderung</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Die **FensterSchließen** -Aktion funktioniert für alle Datenbankobjekte, die der Benutzer explizit öffnen oder schließen kann. Diese Aktion wirkt sich genauso aus, als wenn Sie ein Objekt auswählen und es dann schließen, indem Sie mit der rechten Maustaste auf die Dokumentregisterkarte des Objekts klicken und dann auf **Schließen** im Kontextmenü klicken, oder indem Sie auf die Schaltfläche **Schließen** für das Objekt klicken.

Wenn das Argument **Speichern** auf **Eingabeaufforderung** festgelegt ist und das Objekt vor dem Ausführen der **FensterSchließen** -Aktion noch nicht gespeichert wurde, wird der Benutzer in einem Dialogfeld aufgefordert, das Objekt zu speichern, bevor es vom Makro geschlossen wird. Wenn Sie das Argument **Warnmeldungen An** der **Warnmeldungen** -Aktion auf **Nein** festgelegt haben, wird das Dialogfeld nicht angezeigt, und das Objekt wird automatisch gespeichert.

Verwenden Sie die **CloseWindow** -Methode des **DoCmd** -Objekts, um die **FensterSchließen** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

