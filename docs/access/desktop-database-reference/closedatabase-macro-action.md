---
title: CloseDatabase-Makroaktion
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f08200d2037ab09c8c9aee4ebcc8a98ae228ca2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622494"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase-Makroaktion


**Gilt für**: Access 2013, Office 2013

Sie können die **SchließenDatenbank**-Aktion zum Schließen der aktuellen Datenbank verwenden.

## <a name="setting"></a>Einstellung

Die **SchließenDatenbank**-Aktion weist keine Argumente auf.

## <a name="remarks"></a>Bemerkungen

  - In Access werden keine Aktionen ausgeführt, die in einem Makro auf die **SchließenDatenbank**-Aktion folgen.

  - Diese Aktion hat denselben Effekt wie das Klicken auf die Registerkarte **"Datei"** und dann das Klicken auf **"Datenbank schließen".** Falls beim Ausführen der **SchließenDatenbank** -Aktion nicht gespeicherte Objekte geöffnet sein sollten, entsprechen die angezeigten Dialogfelder denjenigen, die beim Klicken auf **Datenbank schließen** angezeigt werden.

  - Verwenden Sie die **CloseDatabase** -Methode des **DoCmd** -Objekts, um die **SchließenDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

