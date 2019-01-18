---
title: WillMove- und MoveComplete-Ereignisse (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705960"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="1c68a-102">WillMove- und MoveComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="1c68a-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="1c68a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c68a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c68a-p101">Das **WillMove** -Ereignis wird aufgerufen, bevor ein ausstehender Vorgang die aktuelle Position im [Recordset](recordset-object-ado.md)-Objekt ändert. Das **MoveComplete** -Ereignis wird aufgerufen, nachdem die aktuelle Position im **Recordset** -Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1c68a-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c68a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c68a-106">Syntax</span></span>

<span data-ttu-id="1c68a-107">WillMove-*AdReason* *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="1c68a-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="1c68a-108">MoveComplete*AdReason*, *pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="1c68a-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="1c68a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c68a-109">Parameters</span></span>

|<span data-ttu-id="1c68a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c68a-110">Parameter</span></span>|<span data-ttu-id="1c68a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c68a-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1c68a-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="1c68a-112">*adReason*</span></span> |<span data-ttu-id="1c68a-p102">Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Der Wert kann **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** oder **adRsnRequery** sein.</span><span class="sxs-lookup"><span data-stu-id="1c68a-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="1c68a-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="1c68a-115">*pError*</span></span> |<span data-ttu-id="1c68a-p103">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c68a-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="1c68a-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="1c68a-118">*adStatus*</span></span> |<span data-ttu-id="1c68a-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="1c68a-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="1c68a-120">Wird **WillMove** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1c68a-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="1c68a-121">Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="1c68a-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="1c68a-122">Wird **MoveComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1c68a-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="1c68a-123">Legen Sie diesen Parameter vor der Rückgabe von WillMove auf adStatusCancel fest, um den Abbruch des ausstehenden Vorgangs anzufordern. Oder legen Sie diesen Parameter auf adStatusUnwantedEvent fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1c68a-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="1c68a-124">Legen Sie diesen Parameter vor der Rückgabe von **MoveComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1c68a-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="1c68a-125">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="1c68a-125">*pRecordset*</span></span> |<span data-ttu-id="1c68a-p105">Ein [Recordset](recordset-object-ado.md)-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1c68a-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1c68a-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c68a-128">Remarks</span></span>

<span data-ttu-id="1c68a-129">Ein **WillMove** oder **MoveComplete** -Ereignis kann aufgrund der folgenden **Recordset** -Vorgänge auftreten:</span><span class="sxs-lookup"><span data-stu-id="1c68a-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="1c68a-130">Open</span><span class="sxs-lookup"><span data-stu-id="1c68a-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="1c68a-131">Move</span><span class="sxs-lookup"><span data-stu-id="1c68a-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="1c68a-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="1c68a-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1c68a-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="1c68a-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1c68a-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1c68a-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="1c68a-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1c68a-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1c68a-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="1c68a-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="1c68a-137">Requery</span><span class="sxs-lookup"><span data-stu-id="1c68a-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="1c68a-138">Diese Ereignisse können auftreten, wenn die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1c68a-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="1c68a-139">Filter</span><span class="sxs-lookup"><span data-stu-id="1c68a-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="1c68a-140">Index</span><span class="sxs-lookup"><span data-stu-id="1c68a-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="1c68a-141">Lesezeichen</span><span class="sxs-lookup"><span data-stu-id="1c68a-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="1c68a-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="1c68a-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="1c68a-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="1c68a-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="1c68a-144">Diese Ereignisse treten außerdem ein, wenn mit einem untergeordneten **Recordset** -Objekt **Recordset** -Ereignisse verbunden sind und das übergeordnete **Recordset** -Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="1c68a-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="1c68a-145">Sie müssen den  *adStatus*  -Parameter für jeden möglichen **adReason** -Wert auf *adStatusUnwantedEvent* festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem  *adReason*  -Parameter vollständig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1c68a-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

