---
title: Sofortiger Aktualisierungsmodus (Access PC-Datenbank-Referenz)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abc2e8365c60987fedc0d306b274df74c7ee551
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706947"
---
# <a name="immediate-mode"></a>Unmittelbarer Modus


**Betrifft**: Access 2013, Office 2013

Der sofortige Aktualisierungsmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockOptimistic** oder **adLockPessimistic** festgelegt ist. Im sofortigen Aktualisierungsmodus werden Änderungen an einem Datensatz an die Datenquelle weitergegeben, sobald Sie die Bearbeitung einer Zeile als abgeschlossen deklarieren, indem Sie die **Update** -Methode aufrufen.

## <a name="calling-update"></a>Aufrufen der Update-Methode

Wenn Sie den Datensatz verlassen, den Sie hinzufügen oder bearbeiten, bevor Sie die **Update** -Methode aufrufen, ruft ADO zum Speichern der Änderungen automatisch **Update** auf. Sie müssen vor der Navigation die **CancelUpdate** -Methode aufrufen, falls Sie Änderungen am aktuellen Datensatz abbrechen oder einen neu hinzugefügten Datensatz verwerfen möchten.

Der aktuelle Datensatz bleibt aktuell, nachdem Sie die **Update** -Methode aufgerufen haben.

## <a name="cancelupdate"></a>CancelUpdate

Verwenden Sie die **CancelUpdate** -Methode, um Änderungen an der aktuellen Zeile abzubrechen oder um eine neu hinzugefügte Zeile zu verwerfen. Änderungen an der aktuellen Zeile oder eine neue Zeile können nicht abgebrochen werden, nachdem Sie die **Update** -Methode aufgerufen haben, außer die Änderungen sind Teil einer Transaktion, für die Sie ein Rollback mit der **RollbackTrans** -Methode ausführen können, oder Teil einer Batchaktualisierung. Bei einer Batchaktualisierung können Sie **Update** mit der **CancelUpdate** - oder **CancelBatch** -Methode abbrechen.

Wenn Sie beim Aufrufen der **CancelUpdate** -Methode eine neue Zeile hinzufügen, wird die Zeile, die vor dem Aufruf von **AddNew** die aktuelle Zeile war, zur aktuellen Zeile.

Wenn Sie die aktuelle Zeile nicht geändert haben oder keine neue Zeile hinzugefügt haben, wird durch Aufrufen der **CancelUpdate** -Methode ein Fehler generiert.

