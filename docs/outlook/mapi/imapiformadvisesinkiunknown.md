---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792140"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="9c4ad-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c4ad-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="9c4ad-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c4ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c4ad-105">Formular von Servern zum Formular Viewer Benachrichtigungen erhalten können.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c4ad-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9c4ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c4ad-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="9c4ad-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9c4ad-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9c4ad-109">Formular advise-Empfängerobjekten</span><span class="sxs-lookup"><span data-stu-id="9c4ad-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="9c4ad-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9c4ad-111">Formular-Servern</span><span class="sxs-lookup"><span data-stu-id="9c4ad-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="9c4ad-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-112">Called by:</span></span>  <br/> |<span data-ttu-id="9c4ad-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="9c4ad-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="9c4ad-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9c4ad-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9c4ad-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="9c4ad-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9c4ad-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="9c4ad-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9c4ad-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="9c4ad-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9c4ad-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="9c4ad-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="9c4ad-120">Gibt an, dass eine Änderung in den Status des Formular-Viewers aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="9c4ad-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="9c4ad-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="9c4ad-122">Gibt an, ob das Formular die Nachrichtenklasse für die nächste anzuzeigende Meldung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c4ad-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c4ad-123">Remarks</span></span>

<span data-ttu-id="9c4ad-124">Formular Servern mit einem Formular advise-Empfängerobjekt **IMAPIFormAdviseSink** implementieren, anstatt mit ihren Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="9c4ad-125">Aus diesem Grund sollten Formular Viewer erwarten, einen Fehler beim Aufruf von [QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) -Methode des Formulars einen Zeiger auf diese Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="9c4ad-126">Formular Servern rufen Sie einen Viewer [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode für Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="9c4ad-127">Ein Zeiger auf ihre Implementierung **IMAPIFormAdviseSink** ist als Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c4ad-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c4ad-128">See also</span></span>



[<span data-ttu-id="9c4ad-129">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9c4ad-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

