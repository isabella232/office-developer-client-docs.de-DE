---
title: QuitAccess-Makroaktion
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 143ece00d7adb9b4011bd2fe92db069d8beec0e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617706"
---
# <a name="quitaccess-macro-action"></a>QuitAccess-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **BeendenAccess** -Aktion verwenden, um Microsoft Access zu beenden. Für das Speichern von Datenbankobjekten vor dem Beenden von Access kann die **BeendenAccess** -Aktion außerdem mindestens eine Option festlegen.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **BeendenAccess**-Aktion hat das folgende Argument.

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
<td><p><strong>Optionen</strong></p></td>
<td><p>Gibt an, was mit nicht gespeicherten Objekten geschieht, wenn Sie Access beenden. Klicken Sie auf <strong>"Eingabeaufforderung"</strong> (um Dialogfelder anzuzeigen, in denen gefragt wird, ob die einzelnen Objekte gespeichert werden <strong></strong> sollen), <strong>"Alle speichern"</strong> (um alle Objekte ohne Eingabeaufforderung durch Dialogfelder zu speichern) oder <strong>"Beenden"</strong> (beenden, ohne Objekte zu speichern) im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator". Der Standardwert ist <strong>"Alle speichern".</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Access führt keine Aktionen aus, die in einem Makro auf die **BeendenAccess**-Aktion folgen.

Sie können diese Aktion verwenden, um Access ohne Aufforderungen in den Dialogfeldern **Speichern** zu beenden, indem Sie einen benutzerdefinierten Menübefehl oder eine Schaltfläche in einem Formular verwenden. Unter Umständen verfügen Sie über ein Masterformular, das Sie zum Anzeigen der Objekte in Ihrem benutzerdefinierten Arbeitsbereich verwenden. Dieses Formular enthält möglicherweise eine Schaltfläche **Beenden**, mit der ein Makro ausgeführt wird, das die **BeendenAccess** -Aktion enthält, deren Argument **Optionen** auf **Alles speichern** festgelegt ist.

Diese Aktion hat dieselbe Wirkung wie ein Klicken auf die Registerkarte **Datei** und dann ein Klicken auf **Beenden**. Wenn beim Klicken auf diesen Befehl nicht gespeicherte Objekte vorhanden sind, stimmen die Dialogfelder, die angezeigt werden, mit denen überein, die angezeigt werden, wenn Sie **Nachfragen** für das Argument **Optionen** der **BeendenAccess** -Aktion verwenden.

In einem Makro können Sie die **SpeichernObjekt** -Aktion verwenden, um ein angegebenes Objekt zu speichern, ohne Access beenden oder das Objekt schließen zu müssen.

Verwenden Sie die **Quit** -Methode des **DoCmd** -Objekts, um die **BeendenAccess** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

