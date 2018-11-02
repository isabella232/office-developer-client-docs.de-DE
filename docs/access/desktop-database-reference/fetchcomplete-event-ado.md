---
title: FetchComplete-Ereignis (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ae09ff9bfcd694214a63fb630de52260ea7ac31
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925226"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="ffe67-102">FetchComplete-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffe67-102">FetchComplete event (ADO)</span></span>


<span data-ttu-id="ffe67-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffe67-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ffe67-104">Das **FetchComplete** -Ereignis wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das [Recordset](recordset-object-ado.md) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ffe67-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffe67-105">Syntax</span></span>

<span data-ttu-id="ffe67-106">FetchComplete*pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="ffe67-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="ffe67-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffe67-107">Parameters</span></span>

  - <span data-ttu-id="ffe67-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="ffe67-108">*pError*</span></span>

  - <span data-ttu-id="ffe67-p101">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ffe67-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="ffe67-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ffe67-111">*adStatus*</span></span>

  - [<span data-ttu-id="ffe67-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="ffe67-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="ffe67-113">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ffe67-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="ffe67-114">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="ffe67-114">*pRecordset*</span></span>

  - <span data-ttu-id="ffe67-p102">Ein **Recordset** -Objekt. Das Objekt, für das die Datensätze abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ffe67-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe67-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffe67-117">Remarks</span></span>

<span data-ttu-id="ffe67-118">Um **FetchComplete** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ffe67-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

