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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351140"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="467b2-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="467b2-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="467b2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="467b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="467b2-105">Empfängt Benachrichtigungen von Formularen.</span><span class="sxs-lookup"><span data-stu-id="467b2-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="467b2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="467b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="467b2-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="467b2-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="467b2-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="467b2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="467b2-109">Anzeigen von Advise-Senke-Objekten</span><span class="sxs-lookup"><span data-stu-id="467b2-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="467b2-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="467b2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="467b2-111">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="467b2-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="467b2-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="467b2-112">Called by:</span></span>  <br/> |<span data-ttu-id="467b2-113">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="467b2-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="467b2-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="467b2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="467b2-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="467b2-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="467b2-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="467b2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="467b2-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="467b2-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="467b2-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="467b2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="467b2-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="467b2-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="467b2-120">Benachrichtigt den Formular Betrachter darüber, dass ein Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="467b2-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="467b2-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="467b2-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="467b2-122">Benachrichtigt den Formular Betrachter, dass eine neue oder eine vorhandene Nachricht in ein Formular geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="467b2-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="467b2-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="467b2-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="467b2-124">Benachrichtigt den Formular Betrachter über den Druckstatus eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="467b2-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="467b2-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="467b2-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="467b2-126">Benachrichtigt den Formular Betrachter darüber, dass die aktuelle Nachricht an MAPI-Spooler übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="467b2-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="467b2-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="467b2-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="467b2-128">Benachrichtigt den Formular Betrachter darüber, dass die aktuelle Nachricht in einem Formular gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="467b2-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="467b2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="467b2-129">See also</span></span>



[<span data-ttu-id="467b2-130">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="467b2-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

