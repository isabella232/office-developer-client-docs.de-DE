---
title: BeginTransComplete-, CommitTransComplete, RollbackTransComplete-Ereignisse (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702894"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="1c42a-102">BeginTransComplete-, CommitTransComplete- und RollbackTransComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="1c42a-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="1c42a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c42a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c42a-104">Diese Ereignisse werden aufgerufen, nachdem die zugeordnete Operation für das [Connection](connection-object-ado.md)-Objekt die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="1c42a-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="1c42a-105">**BeginTransComplete** wird nach der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1c42a-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="1c42a-106">**CommitTransComplete** wird nach der [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1c42a-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="1c42a-107">**RollbackTransComplete** wird nach der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1c42a-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c42a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c42a-108">Syntax</span></span>

<span data-ttu-id="1c42a-109">BeginTransComplete-*TransactionLevel*, *pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="1c42a-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="1c42a-110">CommitTransComplete-*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="1c42a-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="1c42a-111">RollbackTransComplete*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="1c42a-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="1c42a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c42a-112">Parameters</span></span>

|<span data-ttu-id="1c42a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c42a-113">Parameter</span></span>|<span data-ttu-id="1c42a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c42a-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1c42a-115">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="1c42a-115">*TransactionLevel*</span></span> |<span data-ttu-id="1c42a-116">Ein **Long** -Wert, der die neue Transaktionsebene von **BeginTrans** enthält, das zu diesem Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="1c42a-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="1c42a-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="1c42a-117">*pError*</span></span> |<span data-ttu-id="1c42a-118">Ein [Error](error-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1c42a-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="1c42a-119">Es beschreibt den Fehler, der aufgetreten sind, wenn der Wert von EventStatusEnum **AdStatusErrorsOccurred**ist. Andernfalls wird es nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c42a-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="1c42a-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="1c42a-120">*adStatus*</span></span> |<span data-ttu-id="1c42a-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="1c42a-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="1c42a-122">Diese Ereignisse können nachfolgende Benachrichtigungen verhindern, indem dieser Parameter auf **AdStatusUnwantedEvent** festgelegt wird, bevor das Ereignis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c42a-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="1c42a-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="1c42a-123">*pConnection*</span></span> |<span data-ttu-id="1c42a-124">Das **Connection** -Objekt, für das dieses Ereignis auftrat.</span><span class="sxs-lookup"><span data-stu-id="1c42a-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1c42a-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c42a-125">Remarks</span></span>

<span data-ttu-id="1c42a-126">In Visual C++ können mehrere **Verbindungen** gleichen Ereignisbehandlung Methode freigeben.</span><span class="sxs-lookup"><span data-stu-id="1c42a-126">In Visual C++, multiple **Connections** can share the same event handling method.</span></span> <span data-ttu-id="1c42a-127">Die-Methode verwendet das zurückgegebene **Connection** -Objekt, um zu bestimmen, welches Objekt das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="1c42a-127">The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="1c42a-p104">Wenn die [Attributes](attributes-property-ado.md)-Eigenschaft auf **adXactCommitRetaining** oder **adXactAbortRetaining** festgelegt ist, beginnt nach dem Commit oder Rollback eine neue Transaktion. Verwenden Sie das **BeginTransComplete** -Ereignis, um alle Transaktionsstartereignisse, mit Ausnahme des ersten, zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="1c42a-p104">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

