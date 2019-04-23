---
title: MinimizeWindow-Makroaktion
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9f7c4ab535010dc0329673fd04721615f6eb3cd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288883"
---
# <a name="minimizewindow-macro-action"></a>MinimizeWindow-Makroaktion

**Gilt für**: Access 2013, Office 2013

Wenn der Zugriff auf überlappende Fenster anstelle von Dokumenten im Registerkartenformat konfiguriert ist, können Sie die **minimierenfenster** -Aktion verwenden, um das aktive Fenster auf eine kleine Titelleiste am unteren Rand des Access-Fensters zu reduzieren.

> [!NOTE]
> Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur **WindowState**-Eigenschaft.

## <a name="setting"></a>Einstellung

Die **MinimierenFenster**-Aktion hat keine Argumente.

## <a name="remarks"></a>Bemerkungen

Sie können diese Aktion verwenden, um ein Fenster vom Bildschirm zu entfernen, während das Objekt geöffnet bleibt. Sie können diese Aktion auch verwenden, um ein Objekt zu öffnen, ohne sein Fenster anzuzeigen. Zum Anzeigen des Objekts verwenden Sie die **AuswählenObjekt** -Aktion mit der Aktion **MaximierenFenster** oder **WiederherstellenFenster**. Durch die **WiederherstellenFenster** -Aktion wird ein minimiertes Fenster in seiner vorherigen Größe wiederhergestellt.

The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.

**Tipps**

- Wenn das Fenster, das Sie minimieren möchten, nicht das aktive Fenster ist, müssen Sie zuerst die **AuswählenObjekt** -Aktion verwenden.

- To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.

- Sie können das aktive Fenster ausblenden, indem Sie auf im Menü **Ansicht** auf **Dieses Fenster verwalten**und dann auf **Ausblenden** klicken. Anstatt auf die Größe eines Symbols verkleinert zu werden, wird das Fenster in diesem Fall unsichtbar. Verwenden Sie den Befehl **Einblenden** im gleichen Menü, damit das Fenster wieder angezeigt wird. Mithilfe der **AusführenMenübefehl** -Aktion können Sie jeden dieser Befehle auch in einem Makro ausführen.

- Sie können auch die **SetzenWert** -Aktion verwenden, um die **Sichtbar**-Eigenschaft eines Formulars so festzulegen, dass das Fenster des Formulars ausgeblendet oder angezeigt wird.

Verwenden Sie die **Minimize** -Methode des **DoCmd** -Objekts, um die **MinimierenFenster** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

