---
title: Batch Modus (Access Desktop Database Reference)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296878"
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

