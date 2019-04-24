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
# <a name="batch-mode"></a><span data-ttu-id="c9a3a-102">Batchmodus</span><span class="sxs-lookup"><span data-stu-id="c9a3a-102">Batch mode</span></span>

<span data-ttu-id="c9a3a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9a3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9a3a-p101">Der Batchmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockBatchOptimistic** festgelegt ist und die Batchaktualisierung vom Anbieter unterstützt wird. Bestimmte Sperrtypeinstellungen sind je nach Cursorplatzierung nicht verfügbar. Beispielsweise ist der pessimistische Sperrtyp nicht verfügbar, wenn **CursorLocation** auf **adUseClient** festgelegt ist. Entsprechend unterstützt ein Anbieter möglicherweise keine optimistische Batchsperre, wenn der Cursor auf dem Server platziert ist. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="c9a3a-p102">Mit der **UpdateBatch** -Methode werden Änderungen am **Recordset** -Objekt, die im Kopierpuffer gespeichert sind, an den Server gesendet, um die Datenquelle zu aktualisieren. Im folgenden Abschnitt werden Sie ein **Recordset** -Objekt im Batchmodus öffnen, den Kopierpuffer ändern und dann die Änderungen an die Datenquelle senden, indem Sie **UpdateBatch** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="c9a3a-111">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c9a3a-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="c9a3a-112">Senden von Updates: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="c9a3a-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="c9a3a-113">Filtern nach aktualisierten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="c9a3a-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="c9a3a-114">Umgang mit fehlgeschlagenen Updates</span><span class="sxs-lookup"><span data-stu-id="c9a3a-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="c9a3a-115">Erkennen und Lösen von Konflikten</span><span class="sxs-lookup"><span data-stu-id="c9a3a-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="c9a3a-116">Trennen und erneutes Verbinden des Recordsets</span><span class="sxs-lookup"><span data-stu-id="c9a3a-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="c9a3a-117">Aktualisieren von verknüpften Ergebnissen: Eindeutige Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9a3a-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

