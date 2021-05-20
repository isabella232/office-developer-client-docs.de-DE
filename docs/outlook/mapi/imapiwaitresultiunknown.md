---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062039"
---
# <a name="imapiwaitresult--iunknown"></a><span data-ttu-id="7ee0d-103">IMAPIWaitResult : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ee0d-103">IMAPIWaitResult : IUnknown</span></span>
  
<span data-ttu-id="7ee0d-104">**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="7ee0d-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="7ee0d-105">Diese Schnittstelle wird von Verbrauchern von IMAPIInitMonitor verwendet, um zu steuern, wo das Warten erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7ee0d-105">This interface is used by consumers of IMAPIInitMonitor to control where the wait happens.</span></span> <span data-ttu-id="7ee0d-106">Es ermöglicht ihnen, das Objekt in einem Thread zu erstellen und es in einen anderen Thread zu verschieben, um das tatsächliche Warten durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="7ee0d-106">It allows them create the object on one thread and move it another thread to perform the actual wait.</span></span>

## <a name="vtable-order"></a><span data-ttu-id="7ee0d-107">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="7ee0d-107">Vtable order</span></span>

| <span data-ttu-id="7ee0d-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="7ee0d-108">function</span></span> | <span data-ttu-id="7ee0d-109">description</span><span class="sxs-lookup"><span data-stu-id="7ee0d-109">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="7ee0d-110">HRESULT IMAPIWaitResult::End()</span><span class="sxs-lookup"><span data-stu-id="7ee0d-110">HRESULT IMAPIWaitResult::End()</span></span>](imapiwaitresult-end.md)|<span data-ttu-id="7ee0d-111">Wird aufgerufen, um das Blockieren des Threads zu initiieren, in dem er aufgerufen wird. Dabei muss es sich nicht um denselben Thread wie *IMAPIInitMonitor::BeginWait handelt.*</span><span class="sxs-lookup"><span data-stu-id="7ee0d-111">Called to initiate the blocking wait on the thread where it is called, which does not need to be the same thread that called *IMAPIInitMonitor::BeginWait*.</span></span>|

| <span data-ttu-id="7ee0d-112">Schnellinfos</span><span class="sxs-lookup"><span data-stu-id="7ee0d-112">quick info</span></span> | <span data-ttu-id="7ee0d-113">result</span><span class="sxs-lookup"><span data-stu-id="7ee0d-113">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="7ee0d-114">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="7ee0d-114">Inherits from:</span></span>  <br/> |<span data-ttu-id="7ee0d-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ee0d-115">IUnknown</span></span>  <br/> |
|<span data-ttu-id="7ee0d-116">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7ee0d-116">Implemented by:</span></span>  <br/> |  <span data-ttu-id="7ee0d-117">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="7ee0d-117">OLMAPI32.DLL</span></span><br/> |
|<span data-ttu-id="7ee0d-118">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7ee0d-118">Called by:</span></span>  <br/> |<span data-ttu-id="7ee0d-119">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="7ee0d-119">Client applications</span></span>  <br/> |
|<span data-ttu-id="7ee0d-120">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="7ee0d-120">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7ee0d-121">IID_IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="7ee0d-121">IID_IMAPIWaitResult</span></span>  <br/> |

## <a name="see-also"></a><span data-ttu-id="7ee0d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ee0d-122">See also</span></span>

[<span data-ttu-id="7ee0d-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="7ee0d-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="7ee0d-124">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="7ee0d-124">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="7ee0d-125">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ee0d-125">IMAPIInitMonitor : IUnknown</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="7ee0d-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="7ee0d-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
