---
title: WillChangeRecordset- und RecordsetChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f9126005d8f11f859a3f45cbfec08e6612b59ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473645"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="16ce4-102">WillChangeRecordset- und RecordsetChangeComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="16ce4-102">WillChangeRecordset and RecordsetChangeComplete Events (ADO)</span></span>


<span data-ttu-id="16ce4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="16ce4-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="16ce4-p101">Das **WillChangeRecordset** -Ereignis wird aufgerufen, bevor ein ausstehender Vorgang das [Recordset](recordset-object-ado.md)-Objekt ändert. Das **RecordsetChangeComplete** -Ereignis wird aufgerufen, nachdem das **Recordset** -Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="16ce4-p101">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md). The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ce4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16ce4-106">Syntax</span></span>

<span data-ttu-id="16ce4-107">WillChangeRecordset-*AdReason* *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="16ce4-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="16ce4-108">RecordsetChangeComplete*AdReason*, *pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="16ce4-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="16ce4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16ce4-109">Parameters</span></span>

  - <span data-ttu-id="16ce4-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="16ce4-110">*adReason*</span></span>

  - <span data-ttu-id="16ce4-p102">Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Der Wert kann **adRsnRequery**, **adRsnResynch**, **adRsnClose** oder **adRsnOpen** sein.</span><span class="sxs-lookup"><span data-stu-id="16ce4-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>

  - <span data-ttu-id="16ce4-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="16ce4-113">*adStatus*</span></span>

  - [<span data-ttu-id="16ce4-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="16ce4-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="16ce4-p103">Wird **WillChangeRecordset** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="16ce4-p103">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="16ce4-117">Wird **RecordsetChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist. Oder er wird auf **adStatusCancel** festgelegt, wenn der dem zuvor angenommenen **WillChangeRecordset** -Ereignis zugeordnete Vorgang abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="16ce4-117">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span>
    
    <span data-ttu-id="16ce4-118">Legen Sie diesen Parameter vor der Rückgabe von WillChangeRecordset auf adStatusCancel fest, um den Abbruch des ausstehenden Vorgangs anzufordern. Oder legen Sie diesen Parameter auf adStatusUnwantedEvent fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="16ce4-118">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span>
    
    <span data-ttu-id="16ce4-119">Legen Sie diesen Parameter vor der Rückgabe von **WillChangeRecordset** oder **RecordsetChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="16ce4-119">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="16ce4-120">*pError*</span><span class="sxs-lookup"><span data-stu-id="16ce4-120">*pError*</span></span>

  - <span data-ttu-id="16ce4-p104">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16ce4-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="16ce4-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="16ce4-123">*pRecordset*</span></span>

  - <span data-ttu-id="16ce4-p105">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="16ce4-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="16ce4-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16ce4-126">Remarks</span></span>

<span data-ttu-id="16ce4-127">Ein **WillChangeRecordset** oder **RecordsetChangeComplete** -Ereignis kann aufgrund der Methoden **Recordset** [Requery](requery-method-ado.md) oder [Open](open-method-ado-recordset.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="16ce4-127">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="16ce4-p106">Wenn der Anbieter Textmarken nicht unterstützt, tritt immer eine **RecordsetChange** -Ereignisbenachrichtigung auf, wenn neue Zeilen vom Anbieter abgerufen werden. Die Häufigkeit dieses Ereignisses hängt von der **RecordsetCacheSize** -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="16ce4-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="16ce4-130">Sie müssen den  **adStatus**  -Parameter für jeden möglichen **adReason** -Wert auf **adStatusUnwantedEvent** festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem  **adReason**  -Parameter vollständig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="16ce4-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>

