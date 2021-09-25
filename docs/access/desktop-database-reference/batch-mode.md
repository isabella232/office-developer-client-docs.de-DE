---
title: Batchmodus (Access-Desktopdatenbankreferenz)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5913407ab7071d2f6664a1a22d60911a63479231
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558849"
---
# <a name="batch-mode"></a>Batchmodus

**Gilt für**: Access 2013, Office 2013

Der Batchmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockBatchOptimistic** festgelegt ist und die Batchaktualisierung vom Anbieter unterstützt wird. Bestimmte Sperrtypeinstellungen sind je nach Cursorplatzierung nicht verfügbar. Beispielsweise ist der pessimistische Sperrtyp nicht verfügbar, wenn **CursorLocation** auf **adUseClient** festgelegt ist. Entsprechend unterstützt ein Anbieter möglicherweise keine optimistische Batchsperre, wenn der Cursor auf dem Server platziert ist. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.

Mit der **UpdateBatch** -Methode werden Änderungen am **Recordset** -Objekt, die im Kopierpuffer gespeichert sind, an den Server gesendet, um die Datenquelle zu aktualisieren. Im folgenden Abschnitt werden Sie ein **Recordset** -Objekt im Batchmodus öffnen, den Kopierpuffer ändern und dann die Änderungen an die Datenquelle senden, indem Sie **UpdateBatch** aufrufen.

Dieser Abschnitt enthält die folgenden Themen:

- [Senden von Updates: UpdateBatch](sending-the-updates-updatebatch.md)
- [Filtern nach aktualisierten Datensätzen](filtering-for-updated-records.md)
- [Umgang mit fehlgeschlagenen Updates](dealing-with-failed-updates.md)
- [Erkennen und Lösen von Konflikten](detecting-and-resolving-conflicts.md)
- [Trennen und erneutes Verbinden des Recordsets](disconnecting-and-reconnecting-the-recordset.md)
- [Aktualisieren von verknüpften Ergebnissen: Eindeutige Tabelle](updating-joined-results-unique-table.md)

