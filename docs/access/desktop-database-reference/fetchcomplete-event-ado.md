---
title: FetchComplete-Ereignis (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474720"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="d0b0f-102">FetchComplete-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="d0b0f-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="d0b0f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0b0f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d0b0f-104">Das **FetchComplete** -Ereignis wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das [Recordset](recordset-object-ado.md) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d0b0f-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0b0f-105">Syntax</span></span>

<span data-ttu-id="d0b0f-106">FetchComplete*pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="d0b0f-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="d0b0f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0b0f-107">Parameters</span></span>

  - <span data-ttu-id="d0b0f-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="d0b0f-108">*pError*</span></span>

  - <span data-ttu-id="d0b0f-p101">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d0b0f-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="d0b0f-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="d0b0f-111">*adStatus*</span></span>

  - [<span data-ttu-id="d0b0f-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="d0b0f-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="d0b0f-113">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d0b0f-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="d0b0f-114">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="d0b0f-114">*pRecordset*</span></span>

  - <span data-ttu-id="d0b0f-p102">Ein **Recordset** -Objekt. Das Objekt, für das die Datensätze abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d0b0f-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b0f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0b0f-117">Remarks</span></span>

<span data-ttu-id="d0b0f-118">Um **FetchComplete** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0b0f-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

