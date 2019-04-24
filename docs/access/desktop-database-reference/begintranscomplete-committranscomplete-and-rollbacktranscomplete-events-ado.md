---
title: BeginTransComplete-, CommitTransComplete-, RollbackTransComplete--Ereignisse (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296822"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="f80f7-102">BeginTransComplete-, CommitTransComplete-und RollbackTransComplete--Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="f80f7-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="f80f7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f80f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f80f7-104">Diese Ereignisse werden aufgerufen, nachdem die zugeordnete Operation für das [Connection](connection-object-ado.md)-Objekt die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="f80f7-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="f80f7-105">**BeginTransComplete** wird nach der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f80f7-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="f80f7-106">**CommitTransComplete** wird nach der [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f80f7-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="f80f7-107">**RollbackTransComplete** wird nach der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f80f7-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f80f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f80f7-108">Syntax</span></span>

<span data-ttu-id="f80f7-109">BeginTransComplete*TransactionLevel*, *pError*, \*\* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f80f7-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="f80f7-110">CommitTransComplete*pError*, \*\* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f80f7-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="f80f7-111">RollbackTransComplete-*pError*, \*\* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f80f7-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="f80f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f80f7-112">Parameters</span></span>

|<span data-ttu-id="f80f7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f80f7-113">Parameter</span></span>|<span data-ttu-id="f80f7-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f80f7-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f80f7-115">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="f80f7-115">*TransactionLevel*</span></span> |<span data-ttu-id="f80f7-116">Ein **Long** -Wert, der die neue Transaktionsebene von **BeginTrans** enthält, das zu diesem Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="f80f7-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="f80f7-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="f80f7-117">*pError*</span></span> |<span data-ttu-id="f80f7-118">Ein [Error](error-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f80f7-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="f80f7-119">Sie beschreibt den Fehler, der aufgetreten ist, wenn der Wert von EventStatusEnum **adStatusErrorsOccurred festgelegt**ist; Andernfalls wird nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f80f7-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="f80f7-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="f80f7-120">*adStatus*</span></span> |<span data-ttu-id="f80f7-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="f80f7-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="f80f7-122">Diese Ereignisse können nachfolgende Benachrichtigungen verhindern, indem dieser Parameter auf **AdStatusUnwantedEvent** festgelegt wird, bevor das Ereignis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f80f7-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="f80f7-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="f80f7-123">*pConnection*</span></span> |<span data-ttu-id="f80f7-124">Das **Connection**-Objekt, für das dieses Ereignis auftrat.</span><span class="sxs-lookup"><span data-stu-id="f80f7-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f80f7-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f80f7-125">Remarks</span></span>

<span data-ttu-id="f80f7-p103">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span><span class="sxs-lookup"><span data-stu-id="f80f7-p103">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="f80f7-p104">Wenn die [Attributes](attributes-property-ado.md)-Eigenschaft auf **adXactCommitRetaining** oder **adXactAbortRetaining** festgelegt ist, beginnt nach dem Commit oder Rollback eine neue Transaktion. Verwenden Sie das **BeginTransComplete**-Ereignis, um alle Transaktionsstartereignisse, mit Ausnahme des ersten, zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="f80f7-p104">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

