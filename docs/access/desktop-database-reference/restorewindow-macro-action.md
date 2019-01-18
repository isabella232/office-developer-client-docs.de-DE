---
title: RestoreWindow-Makroaktion
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718833"
---
# <a name="restorewindow-macro-action"></a>RestoreWindow-Makroaktion

**Betrifft**: Access 2013, Office 2013

Um die vorherige Größe eines maximierten oder minimierten Fensters wiederherzustellen, können Sie die **WiederherstellenFenster** -Aktion verwenden.

> [!NOTE]
> [!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur **WindowState** -Eigenschaft.

## <a name="setting"></a>Einstellung

Die **WiederherstellenFenster** -Aktion hat keine Argumente.

## <a name="remarks"></a>Hinweise

Diese Aktion funktioniert für das ausgewählte Objekt. Wenn ein Objekt minimiert worden ist, können Sie es auswählen, indem Sie die **AuswählenObjekt** -Aktion verwenden, und dann seine vorherige Größe wiederherstellen, indem Sie die **WiederherstellenFenster** -Aktion verwenden.

Sie können die **VerschiebenUndGrößeÄndernFenster** -Aktion verwenden, um ein Fenster, das wiederhergestellt wurde, zu verschieben oder in der Größe zu ändern.

Die **WiederherstellenFenster** -Aktion hat dieselbe Wirkung wie ein Klicken auf die Schaltfläche **Wiederherstellen** in der rechten oberen Ecke des Fensters oder ein Klicken auf den Befehl **Wiederherstellen** im Fenstermenü **System**.

Verwenden Sie die **Restore** -Methode des **DoCmd** -Objekts, um die **WiederherstellenFenster** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

