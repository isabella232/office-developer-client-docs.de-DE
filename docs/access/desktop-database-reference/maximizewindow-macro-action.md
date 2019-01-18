---
title: MaximizeWindow-Makroaktion
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715949"
---
# <a name="maximizewindow-macro-action"></a>MaximizeWindow-Makroaktion

**Betrifft**: Access 2013, Office 2013

Wenn überlappende Fenster anstelle von Dokumente im Registerkartenformat verwenden Zugriff konfiguriert ist, können Sie die **Maximierenfenster** -Aktion verwenden, um das aktive Fenster zu vergrößern, damit es das Access-Fenster ausfüllt. Diese Aktion ermöglicht es Ihnen, so viel wie möglich vom Objekt im aktiven Fenster anzuzeigen.

> [!NOTE]
> [!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur **WindowState** -Eigenschaft.

## <a name="setting"></a>Einstellung

Die **MaximierenFenster** -Aktion hat keine Argumente.

## <a name="remarks"></a>Hinweise

Diese Aktion hat dieselbe Wirkung wie das Klicken auf die Schaltfläche **Maximieren** in der oberen rechten Fensterecke oder klicken auf **Maximieren** im **Systemmenü des Fensters** .

Sie können die **WiederherstellenFenster** -Aktion verwenden, um ein maximiertes Fenster in seiner vorherigen Größe wiederherzustellen.

> [!TIP]
> - Wenn das Fenster, das Sie maximieren möchten, nicht das aktive Fenster ist, müssen Sie die **AuswählenObjekt** -Aktion verwenden.
> - Wenn Sie ein Fenster in Access maximieren, werden alle anderen Fenster ebenfalls maximiert, wenn Sie sie öffnen oder zu diesen wechseln. Popupformulare werden jedoch nicht maximiert. Falls ein Formular seine Größe beibehalten soll, wenn andere Fenster maximiert werden, müssen Sie seine **PopUp** -Eigenschaft auf **Ja** festlegen.

Verwenden Sie die **Maximize** -Methode des **DoCmd** -Objekts, um die **MaximierenFenster** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

