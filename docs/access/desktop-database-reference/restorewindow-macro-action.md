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
ms.localizationpriority: medium
ms.openlocfilehash: b70dd9941f5a14dbbb23b5c1bb3939e54e49f2d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593663"
---
# <a name="restorewindow-macro-action"></a>RestoreWindow-Makroaktion

**Gilt für**: Access 2013, Office 2013

Um die vorherige Größe eines maximierten oder minimierten Fensters wiederherzustellen, können Sie die **WiederherstellenFenster**-Aktion verwenden.

> [!NOTE]
> Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur **WindowState**-Eigenschaft.

## <a name="setting"></a>Einstellung

Die **WiederherstellenFenster**-Aktion hat keine Argumente.

## <a name="remarks"></a>HinwBemerkungeneise

Diese Aktion funktioniert für das ausgewählte Objekt. Wenn ein Objekt minimiert worden ist, können Sie es auswählen, indem Sie die **AuswählenObjekt**-Aktion verwenden, und dann seine vorherige Größe wiederherstellen, indem Sie die **WiederherstellenFenster**-Aktion verwenden.

Sie können die **VerschiebenUndGrößeÄndernFenster** -Aktion verwenden, um ein Fenster, das wiederhergestellt wurde, zu verschieben oder in der Größe zu ändern.

Die **WiederherstellenFenster**-Aktion hat dieselbe Wirkung wie ein Klicken auf die Schaltfläche **Wiederherstellen** in der rechten oberen Ecke des Fensters oder ein Klicken auf den Befehl **Wiederherstellen** im Fenstermenü **System**.

Verwenden Sie die **Restore**-Methode des **DoCmd**-Objekts, um die **WiederherstellenFenster**-Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

