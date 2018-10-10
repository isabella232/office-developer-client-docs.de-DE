---
title: Batch-Modus (Access PC-Datenbank-Referenz)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e72997d2484bdfcec91542b0b8de6bbbb23e3fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472816"
---
# <a name="batch-mode"></a>Batchmodus


**Betrifft**: Access 2013 | Office 2013

Der Batchmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockBatchOptimistic** festgelegt ist und die Batchaktualisierung vom Anbieter unterstützt wird. Bestimmte Sperrtypeinstellungen sind je nach Cursorplatzierung nicht verfügbar. Beispielsweise ist der pessimistische Sperrtyp nicht verfügbar, wenn **CursorLocation** auf **adUseClient** festgelegt ist. Entsprechend unterstützt ein Anbieter möglicherweise keine optimistische Batchsperre, wenn der Cursor auf dem Server platziert ist. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.

Mit der **UpdateBatch** -Methode werden Änderungen am **Recordset** -Objekt, die im Kopierpuffer gespeichert sind, an den Server gesendet, um die Datenquelle zu aktualisieren. Im folgenden Abschnitt werden Sie ein **Recordset** -Objekt im Batchmodus öffnen, den Kopierpuffer ändern und dann die Änderungen an die Datenquelle senden, indem Sie **UpdateBatch** aufrufen.

