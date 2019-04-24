---
title: Signalton-Makroaktion (Access Desktop Database Reference)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296864"
---
# <a name="beep-macro-action"></a>Beep-Makroaktion


**Gilt für**: Access 2013, Office 2013

Sie können die **Signalton**-Aktion verwenden, um einen Signalton über den Lautsprecher des Computers auszugeben.

## <a name="setting"></a>Einstellung

Die **Signalton**-Aktion hat keine Argumente.

## <a name="remarks"></a>Bemerkungen

Sie können die **Signalton**-Aktion verwenden, um auf folgende Begebenheiten hinzuweisen:

  - Wichtige Bildschirmänderungen sind aufgetreten.

  - Es wurden die falsche Arten von Daten in ein Steuerelement eingegeben. Beispielsweise hat der Benutzer numerische Daten in ein Textfeld-Steuerelement eingegeben.

  - Ein Makro hat einen angegebenen Punkt erreicht oder seine Aktionen abgeschlossen.

Häufigkeit und Dauer des Signaltons hängen von der Hardware des Computers ab.

Verwenden Sie die **Beep** -Methode des **DoCmd** -Objekts, um die **Signalton** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

