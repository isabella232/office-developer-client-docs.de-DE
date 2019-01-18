---
title: FetchComplete-Ereignis (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701963"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="3a0ba-102">FetchComplete-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a0ba-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="3a0ba-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a0ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a0ba-104">Das **FetchComplete** -Ereignis wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das [Recordset](recordset-object-ado.md) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3a0ba-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a0ba-105">Syntax</span></span>

<span data-ttu-id="3a0ba-106">FetchComplete*pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="3a0ba-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="3a0ba-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a0ba-107">Parameters</span></span>

|<span data-ttu-id="3a0ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a0ba-108">Parameter</span></span>|<span data-ttu-id="3a0ba-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a0ba-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3a0ba-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="3a0ba-110">*pError*</span></span> |<span data-ttu-id="3a0ba-p101">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a0ba-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="3a0ba-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="3a0ba-113">*adStatus*</span></span> |<span data-ttu-id="3a0ba-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="3a0ba-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="3a0ba-115">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3a0ba-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="3a0ba-116">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="3a0ba-116">*pRecordset*</span></span> |<span data-ttu-id="3a0ba-p103">Ein **Recordset** -Objekt. Das Objekt, für das die Datensätze abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3a0ba-p103">A **Recordset** object. The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3a0ba-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a0ba-119">Remarks</span></span>

<span data-ttu-id="3a0ba-120">Um **FetchComplete** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a0ba-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

