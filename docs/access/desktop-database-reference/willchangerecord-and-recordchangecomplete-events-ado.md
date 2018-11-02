---
title: WillChangeRecord- und RecordChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3177e27d3485d8a4ec6adafaa03d968fc15fa62a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925960"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a><span data-ttu-id="0522f-102">WillChangeRecord- und RecordChangeComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="0522f-102">WillChangeRecord and RecordChangeComplete events (ADO)</span></span>


<span data-ttu-id="0522f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0522f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0522f-p101">Das **WillChangeRecord** -Ereignis wird aufgerufen, bevor ein oder mehrere Datensätze (Zeilen) im [Recordset](recordset-object-ado.md)-Objekt geändert werden. Das **RecordChangeComplete** -Ereignis wird aufgerufen, nachdem ein oder mehrere Datensätze geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="0522f-p101">The **WillChangeRecord** event is called before one or more records (rows) in the [Recordset](recordset-object-ado.md) change. The **RecordChangeComplete** event is called after one or more records change.</span></span>

## <a name="syntax"></a><span data-ttu-id="0522f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0522f-106">Syntax</span></span>

<span data-ttu-id="0522f-107">WillChangeRecord-*AdReason*, *cRecords*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="0522f-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="0522f-108">RecordChangeComplete*AdReason*, *cRecords*, *pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="0522f-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="0522f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0522f-109">Parameters</span></span>

  - <span data-ttu-id="0522f-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="0522f-110">*adReason*</span></span>

  - <span data-ttu-id="0522f-p102">Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Sein Wert kann **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** oder **adRsnFirstChange** sein.</span><span class="sxs-lookup"><span data-stu-id="0522f-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, or **adRsnFirstChange**.</span></span>

  - <span data-ttu-id="0522f-113">*cRecords*</span><span class="sxs-lookup"><span data-stu-id="0522f-113">*cRecords*</span></span>

  - <span data-ttu-id="0522f-114">Ein **Long** -Wert, der die Anzahl sich ändernder (betroffener) Datensätze angibt.</span><span class="sxs-lookup"><span data-stu-id="0522f-114">A **Long** value that indicates the number of records changing (affected).</span></span>

  - <span data-ttu-id="0522f-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="0522f-115">*pError*</span></span>

  - <span data-ttu-id="0522f-p103">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0522f-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="0522f-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="0522f-118">*adStatus*</span></span>

  - [<span data-ttu-id="0522f-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="0522f-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="0522f-p104">Wird **WillChangeRecord** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="0522f-p104">When **WillChangeRecord** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="0522f-122">Wird **RecordChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0522f-122">When **RecordChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="0522f-123">Legen Sie diesen Parameter vor der Rückgabe von WillChangeRecord auf adStatusCancel fest, um den Abbruch des dieses Ereignis verursachenden Vorgangs anzufordern. Oder legen Sie diesen Parameter auf adStatusUnwantedEvent fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="0522f-123">Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="0522f-124">Legen Sie diesen Parameter vor der Rückgabe von **RecordChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="0522f-124">Before **RecordChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="0522f-125">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="0522f-125">*pRecordset*</span></span>

  - <span data-ttu-id="0522f-p105">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0522f-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0522f-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0522f-128">Remarks</span></span>

<span data-ttu-id="0522f-129">Ein **WillChangeRecord** - oder ein **RecordChangeComplete** -Ereignis kann aufgrund der folgenden **Recordset** -Vorgänge für das erste geänderte Feld einer Zeile eintreten: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) und [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0522f-129">A **WillChangeRecord** or **RecordChangeComplete** event may occur for the first changed field in a row due to the following **Recordset** operations: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [CancelBatch](cancelbatch-method-ado.md).</span></span> <span data-ttu-id="0522f-130">Der Wert der das **Recordset** [CursorType](cursortype-property-ado.md) bestimmt, welche Vorgänge dazu führen, dass die Ereignisse eintritt.</span><span class="sxs-lookup"><span data-stu-id="0522f-130">The value of the **Recordset** [CursorType](cursortype-property-ado.md) determines which operations cause the events to occur.</span></span>

<span data-ttu-id="0522f-131">Während des **WillChangeRecord** -Ereignisses wird die **Recordset** - [Filter](filter-property-ado.md) -Eigenschaft auf **AdFilterAffectedRecords**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0522f-131">During the **WillChangeRecord** event, the **Recordset** [Filter](filter-property-ado.md) property is set to **adFilterAffectedRecords**.</span></span> <span data-ttu-id="0522f-132">Sie können diese Eigenschaft nicht ändern, während das Ereignis verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0522f-132">You cannot change this property while processing the event.</span></span>

<span data-ttu-id="0522f-133">Sie müssen den adStatus-Parameter für jeden möglichen adReason-Wert auf adStatusUnwantedEvent festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem adReason-Parameter vollständig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0522f-133">You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.</span></span>

