---
title: Batch-Modus (Access PC-Datenbank-Referenz)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37f66f6ef6c4ed63b106584a6ac5118cddf20526
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861203"
---
# <a name="batch-mode"></a><span data-ttu-id="d9423-102">Batchmodus</span><span class="sxs-lookup"><span data-stu-id="d9423-102">Batch Mode</span></span>


<span data-ttu-id="d9423-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9423-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9423-p101">Der Batchmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockBatchOptimistic** festgelegt ist und die Batchaktualisierung vom Anbieter unterstützt wird. Bestimmte Sperrtypeinstellungen sind je nach Cursorplatzierung nicht verfügbar. Beispielsweise ist der pessimistische Sperrtyp nicht verfügbar, wenn **CursorLocation** auf **adUseClient** festgelegt ist. Entsprechend unterstützt ein Anbieter möglicherweise keine optimistische Batchsperre, wenn der Cursor auf dem Server platziert ist. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.</span><span class="sxs-lookup"><span data-stu-id="d9423-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="d9423-p102">Mit der **UpdateBatch** -Methode werden Änderungen am **Recordset** -Objekt, die im Kopierpuffer gespeichert sind, an den Server gesendet, um die Datenquelle zu aktualisieren. Im folgenden Abschnitt werden Sie ein **Recordset** -Objekt im Batchmodus öffnen, den Kopierpuffer ändern und dann die Änderungen an die Datenquelle senden, indem Sie **UpdateBatch** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d9423-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="d9423-111">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="d9423-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="d9423-112">Sending the Updates: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="d9423-112">Sending the Updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)

- [<span data-ttu-id="d9423-113">Filtering for Updated Records</span><span class="sxs-lookup"><span data-stu-id="d9423-113">Filtering for Updated Records</span></span>](filtering-for-updated-records.md)

- [<span data-ttu-id="d9423-114">Dealing with Failed Updates</span><span class="sxs-lookup"><span data-stu-id="d9423-114">Dealing with Failed Updates</span></span>](dealing-with-failed-updates.md)

- [<span data-ttu-id="d9423-115">Detecting and Resolving Conflicts</span><span class="sxs-lookup"><span data-stu-id="d9423-115">Detecting and Resolving Conflicts</span></span>](detecting-and-resolving-conflicts.md)

- [<span data-ttu-id="d9423-116">Disconnecting and Reconnecting the Recordset</span><span class="sxs-lookup"><span data-stu-id="d9423-116">Disconnecting and Reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)

- [<span data-ttu-id="d9423-117">Aktualisieren von verknüpften Ergebnissen: "Unique Table"</span><span class="sxs-lookup"><span data-stu-id="d9423-117">Updating JOINed Results: Unique Table</span></span>](updating-joined-results-unique-table.md)

