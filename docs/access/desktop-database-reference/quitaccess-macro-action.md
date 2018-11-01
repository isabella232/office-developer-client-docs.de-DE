---
title: BeendenAccess-Makroaktion
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d26f8d32e0df350c52ea22dfec44ac7a24c9ecc9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870751"
---
# <a name="quitaccess-macro-action"></a>BeendenAccess-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **BeendenAccess** -Aktion verwenden, um Microsoft Access zu beenden. Für das Speichern von Datenbankobjekten vor dem Beenden von Access kann die **BeendenAccess** -Aktion außerdem mindestens eine Option festlegen.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **BeendenAccess** -Aktion hat das folgende Argument.

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
<td><p><strong>Options</strong></p></td>
<td><p>Gibt an, was mit nicht gespeicherten Objekten geschieht, wenn Sie Access beenden. Klicken Sie im Feld Optionen im Bereich Aktionsargumente des Bereichs Makro-Generator auf Nachfragen (um Dialogfelder anzuzeigen, die Sie fragen, ob Sie ein Objekt speichern möchten), Alles speichern (um alle Objekte zu speichern, ohne anhand von Dialogfeldern gefragt zu werden) oder auf Beenden (um zu beenden, ohne die Objekte zu speichern). Die Standardeinstellung ist Alles speichern.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Access führt keine Aktionen aus, die in einem Makro auf die **BeendenAccess** -Aktion folgen.

Sie können diese Aktion verwenden, um Access ohne Aufforderungen in den Dialogfeldern **Speichern** zu beenden, indem Sie einen benutzerdefinierten Menübefehl oder eine Schaltfläche in einem Formular verwenden. Unter Umständen verfügen Sie über ein Masterformular, das Sie zum Anzeigen der Objekte in Ihrem benutzerdefinierten Arbeitsbereich verwenden. Dieses Formular enthält möglicherweise eine Schaltfläche **Beenden**, mit der ein Makro ausgeführt wird, das die **BeendenAccess** -Aktion enthält, deren Argument **Optionen** auf **Alles speichern** festgelegt ist.

Diese Aktion hat dieselbe Wirkung wie ein Klicken auf die Registerkarte **Datei** und dann ein Klicken auf **Beenden**. Wenn beim Klicken auf diesen Befehl nicht gespeicherte Objekte vorhanden sind, stimmen die Dialogfelder, die angezeigt werden, mit denen überein, die angezeigt werden, wenn Sie **Nachfragen** für das Argument **Optionen** der **BeendenAccess** -Aktion verwenden.

In einem Makro können Sie die **SpeichernObjekt** -Aktion verwenden, um ein angegebenes Objekt zu speichern, ohne Access beenden oder das Objekt schließen zu müssen.

Verwenden Sie die **Quit** -Methode des **DoCmd** -Objekts, um die **BeendenAccess** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

