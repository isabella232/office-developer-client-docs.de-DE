---
title: BeginTransComplete-, CommitTransComplete, RollbackTransComplete-Ereignisse (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf38a106a8cb53c1603628f0c3c0096be4b73d52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888636"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="b7a9d-102">BeginTransComplete-, CommitTransComplete- und RollbackTransComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="b7a9d-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)</span></span>


<span data-ttu-id="b7a9d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7a9d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b7a9d-104">Diese Ereignisse werden aufgerufen, nachdem die zugeordnete Operation für das [Connection](connection-object-ado.md)-Objekt die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

  - <span data-ttu-id="b7a9d-105">**BeginTransComplete** wird nach der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="b7a9d-106">**CommitTransComplete** wird nach der [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="b7a9d-107">**RollbackTransComplete** wird nach der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7a9d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7a9d-108">Syntax</span></span>

<span data-ttu-id="b7a9d-109">BeginTransComplete-*TransactionLevel*, *pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="b7a9d-110">CommitTransComplete-*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="b7a9d-111">RollbackTransComplete*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="b7a9d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7a9d-112">Parameters</span></span>

  - <span data-ttu-id="b7a9d-113">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-113">*TransactionLevel*</span></span>

  - <span data-ttu-id="b7a9d-114">Ein **Long** -Wert, der die neue Transaktionsebene von **BeginTrans** enthält, das zu diesem Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-114">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>

  - <span data-ttu-id="b7a9d-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-115">*pError*</span></span>

  - <span data-ttu-id="b7a9d-p101">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der Wert von EventStatusEnum **adStatusErrorsOccurred** lautet; andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="b7a9d-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-118">*adStatus*</span></span>

  - [<span data-ttu-id="b7a9d-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="b7a9d-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="b7a9d-120">Diese Ereignisse können nachfolgende Benachrichtigungen verhindern, indem dieser Parameter auf **AdStatusUnwantedEvent** festgelegt wird, bevor das Ereignis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-120">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>

  - <span data-ttu-id="b7a9d-121">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="b7a9d-121">*pConnection*</span></span>

  - <span data-ttu-id="b7a9d-122">Das **Connection** -Objekt, für das dieses Ereignis auftrat.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-122">The **Connection** object for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7a9d-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7a9d-123">Remarks</span></span>

<span data-ttu-id="b7a9d-124">In Visual C++ können mehrere **Verbindungen** gleichen Ereignisbehandlung Methode freigeben.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-124">In Visual C++, multiple **Connections** can share the same event handling method.</span></span> <span data-ttu-id="b7a9d-125">Die-Methode verwendet das zurückgegebene **Connection** -Objekt, um zu bestimmen, welches Objekt das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-125">The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="b7a9d-p103">Wenn die [Attributes](attributes-property-ado.md)-Eigenschaft auf **adXactCommitRetaining** oder **adXactAbortRetaining** festgelegt ist, beginnt nach dem Commit oder Rollback eine neue Transaktion. Verwenden Sie das **BeginTransComplete** -Ereignis, um alle Transaktionsstartereignisse, mit Ausnahme des ersten, zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-p103">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

