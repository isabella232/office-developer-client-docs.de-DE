---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792483"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="4a1d7-103">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a1d7-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="4a1d7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a1d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a1d7-105">Er empfängt Benachrichtigungen von Formularen.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a1d7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4a1d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a1d7-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="4a1d7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4a1d7-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="4a1d7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4a1d7-109">Empfängerobjekten advise-Ansicht</span><span class="sxs-lookup"><span data-stu-id="4a1d7-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="4a1d7-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4a1d7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a1d7-111">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="4a1d7-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="4a1d7-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4a1d7-112">Called by:</span></span>  <br/> |<span data-ttu-id="4a1d7-113">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="4a1d7-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="4a1d7-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="4a1d7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4a1d7-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4a1d7-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="4a1d7-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="4a1d7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4a1d7-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="4a1d7-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4a1d7-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="4a1d7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4a1d7-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="4a1d7-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="4a1d7-120">Benachrichtigt dem Formular-Viewer, dass ein Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="4a1d7-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="4a1d7-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="4a1d7-122">Benachrichtigt dem Formular-Viewer, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="4a1d7-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="4a1d7-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="4a1d7-124">Benachrichtigt den Formular-Viewer des Status eines Formulars drucken.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="4a1d7-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="4a1d7-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="4a1d7-126">Benachrichtigt dem Formular-Viewer, dass die aktuelle Nachricht zu MAPI-Warteschlange gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="4a1d7-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="4a1d7-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="4a1d7-128">Benachrichtigt den Formular-Viewer, den die aktuelle Nachricht in einem Formular gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a1d7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a1d7-129">See also</span></span>



[<span data-ttu-id="4a1d7-130">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4a1d7-130">MAPI Interfaces</span></span>](mapi-interfaces.md)
