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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 157703fc9702bb954b4a5c570fc3d5c045e181cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567188"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="4fe22-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fe22-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="4fe22-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fe22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fe22-105">Er empfängt Benachrichtigungen von Formularen.</span><span class="sxs-lookup"><span data-stu-id="4fe22-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fe22-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4fe22-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fe22-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="4fe22-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4fe22-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="4fe22-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4fe22-109">Empfängerobjekten advise-Ansicht</span><span class="sxs-lookup"><span data-stu-id="4fe22-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="4fe22-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4fe22-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4fe22-111">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="4fe22-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="4fe22-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4fe22-112">Called by:</span></span>  <br/> |<span data-ttu-id="4fe22-113">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="4fe22-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="4fe22-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="4fe22-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4fe22-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4fe22-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="4fe22-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="4fe22-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4fe22-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="4fe22-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4fe22-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="4fe22-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4fe22-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="4fe22-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="4fe22-120">Benachrichtigt dem Formular-Viewer, dass ein Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4fe22-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="4fe22-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="4fe22-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="4fe22-122">Benachrichtigt dem Formular-Viewer, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4fe22-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="4fe22-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="4fe22-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="4fe22-124">Benachrichtigt den Formular-Viewer des Status eines Formulars drucken.</span><span class="sxs-lookup"><span data-stu-id="4fe22-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="4fe22-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="4fe22-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="4fe22-126">Benachrichtigt dem Formular-Viewer, dass die aktuelle Nachricht zu MAPI-Warteschlange gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4fe22-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="4fe22-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="4fe22-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="4fe22-128">Benachrichtigt den Formular-Viewer, den die aktuelle Nachricht in einem Formular gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="4fe22-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fe22-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fe22-129">See also</span></span>



[<span data-ttu-id="4fe22-130">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4fe22-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

