---
title: CloseDatabase-Makroaktion
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714437"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **SchließenDatenbank** -Aktion zum Schließen der aktuellen Datenbank verwenden.

## <a name="setting"></a>Einstellung

Die **SchließenDatenbank** -Aktion weist keine Argumente auf.

## <a name="remarks"></a>Hinweise

  - In Access werden keine Aktionen ausgeführt, die in einem Makro auf die **SchließenDatenbank** -Aktion folgen.

  - Diese Aktion hat dieselbe Wirkung wie das Klicken auf die Registerkarte **Datei** , und klicken Sie dann auf **Datenbank schließen**. Falls beim Ausführen der **SchließenDatenbank** -Aktion nicht gespeicherte Objekte geöffnet sein sollten, entsprechen die angezeigten Dialogfelder denjenigen, die beim Klicken auf **Datenbank schließen** angezeigt werden.

  - Verwenden Sie die **CloseDatabase** -Methode des **DoCmd** -Objekts, um die **SchließenDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

