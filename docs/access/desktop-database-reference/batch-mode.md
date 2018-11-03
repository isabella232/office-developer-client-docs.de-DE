---
title: Batch-Modus (Access PC-Datenbank-Referenz)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9541e8b7888f5fb5f16bcfb343d545cf304b1afd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945789"
---
# <a name="batch-mode"></a>Im Batchmodus

**Betrifft**: Access 2013, Office 2013

Der Batchmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockBatchOptimistic** festgelegt ist und die Batchaktualisierung vom Anbieter unterstützt wird. Bestimmte Sperrtypeinstellungen sind je nach Cursorplatzierung nicht verfügbar. Beispielsweise ist der pessimistische Sperrtyp nicht verfügbar, wenn **CursorLocation** auf **adUseClient** festgelegt ist. Entsprechend unterstützt ein Anbieter möglicherweise keine optimistische Batchsperre, wenn der Cursor auf dem Server platziert ist. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.

Mit der **UpdateBatch** -Methode werden Änderungen am **Recordset** -Objekt, die im Kopierpuffer gespeichert sind, an den Server gesendet, um die Datenquelle zu aktualisieren. Im folgenden Abschnitt werden Sie ein **Recordset** -Objekt im Batchmodus öffnen, den Kopierpuffer ändern und dann die Änderungen an die Datenquelle senden, indem Sie **UpdateBatch** aufrufen.

Dieser Abschnitt enthält die folgenden Themen:

- [Senden der Aktualisierungen: UpdateBatch](sending-the-updates-updatebatch.md)
- [Filtern nach aktualisierten Datensätzen](filtering-for-updated-records.md)
- [Umgehen mit fehlgeschlagenen Aktualisierungen](dealing-with-failed-updates.md)
- [Erkennen und Lösen von Konflikten](detecting-and-resolving-conflicts.md)
- [Trennen und Wiederherstellen der Verbindung für des Recordset-Objekts](disconnecting-and-reconnecting-the-recordset.md)
- [Aktualisieren von Ergebnissen beigetreten: Unique Table](updating-joined-results-unique-table.md)

