---
title: WillMove- und MoveComplete-Ereignisse (ADO)
TOCTitle: WillMove and MoveComplete Events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 875b9825b1482bbd33808cafc6df626b2e78b81b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473417"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="ee147-102">WillMove- und MoveComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="ee147-102">WillMove and MoveComplete Events (ADO)</span></span>


<span data-ttu-id="ee147-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee147-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ee147-p101">Das **WillMove** -Ereignis wird aufgerufen, bevor ein ausstehender Vorgang die aktuelle Position im [Recordset](recordset-object-ado.md)-Objekt ändert. Das **MoveComplete** -Ereignis wird aufgerufen, nachdem die aktuelle Position im **Recordset** -Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ee147-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee147-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee147-106">Syntax</span></span>

<span data-ttu-id="ee147-107">WillMove-*AdReason* *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="ee147-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="ee147-108">MoveComplete*AdReason*, *pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="ee147-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="ee147-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee147-109">Parameters</span></span>

  - <span data-ttu-id="ee147-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="ee147-110">*adReason*</span></span>

  - <span data-ttu-id="ee147-p102">Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Der Wert kann **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** oder **adRsnRequery** sein.</span><span class="sxs-lookup"><span data-stu-id="ee147-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="ee147-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="ee147-113">*pError*</span></span>

  - <span data-ttu-id="ee147-p103">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee147-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="ee147-116">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ee147-116">*adStatus*</span></span>

  - [<span data-ttu-id="ee147-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="ee147-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="ee147-p104">Wird **WillMove** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="ee147-p104">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="ee147-120">Wird **MoveComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="ee147-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="ee147-121">Legen Sie diesen Parameter vor der Rückgabe von WillMove auf adStatusCancel fest, um den Abbruch des ausstehenden Vorgangs anzufordern. Oder legen Sie diesen Parameter auf adStatusUnwantedEvent fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ee147-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="ee147-122">Legen Sie diesen Parameter vor der Rückgabe von **MoveComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ee147-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="ee147-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="ee147-123">*pRecordset*</span></span>

  - <span data-ttu-id="ee147-p105">Ein [Recordset](recordset-object-ado.md)-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ee147-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee147-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee147-126">Remarks</span></span>

<span data-ttu-id="ee147-p106">Ein **WillMove** -Ereignis oder ein **MoveComplete** -Ereignis kann aufgrund der folgenden **Recordset** -Vorgänge eintreten: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) und [Requery](requery-method-ado.md). Diese Ereignisse können aufgrund der folgenden Eigenschaften eintreten: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) und [AbsolutePosition](absoluteposition-property-ado.md). Diese Ereignisse treten außerdem ein, wenn mit einem untergeordneten **Recordset** -Objekt **Recordset** -Ereignisse verbunden sind und das übergeordnete **Recordset** -Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ee147-p106">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md). These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md). These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="ee147-130">Sie müssen den  **adStatus**  -Parameter für jeden möglichen **adReason** -Wert auf adStatusUnwantedEvent festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem  adReason  -Parameter vollständig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ee147-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>

