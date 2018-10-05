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
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392060"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="dd171-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd171-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="dd171-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd171-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd171-105">Formular von Servern zum Formular Viewer Benachrichtigungen erhalten können.</span><span class="sxs-lookup"><span data-stu-id="dd171-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd171-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="dd171-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd171-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="dd171-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="dd171-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="dd171-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dd171-109">Formular advise-Empfängerobjekten</span><span class="sxs-lookup"><span data-stu-id="dd171-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="dd171-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dd171-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd171-111">Formular-Servern</span><span class="sxs-lookup"><span data-stu-id="dd171-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="dd171-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dd171-112">Called by:</span></span>  <br/> |<span data-ttu-id="dd171-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="dd171-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="dd171-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="dd171-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dd171-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dd171-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="dd171-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="dd171-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dd171-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="dd171-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dd171-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="dd171-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dd171-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="dd171-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="dd171-120">Gibt an, dass eine Änderung in den Status des Formular-Viewers aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="dd171-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="dd171-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="dd171-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="dd171-122">Gibt an, ob das Formular die Nachrichtenklasse für die nächste anzuzeigende Meldung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="dd171-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd171-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd171-123">Remarks</span></span>

<span data-ttu-id="dd171-124">Formular Servern mit einem Formular advise-Empfängerobjekt **IMAPIFormAdviseSink** implementieren, anstatt mit ihren Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dd171-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="dd171-125">Aus diesem Grund sollten Formular Viewer erwarten, einen Fehler beim Aufruf von [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode des Formulars einen Zeiger auf diese Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="dd171-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="dd171-126">Formular Servern rufen Sie einen Viewer [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode für Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="dd171-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="dd171-127">Ein Zeiger auf ihre Implementierung **IMAPIFormAdviseSink** ist als Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd171-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd171-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd171-128">See also</span></span>



[<span data-ttu-id="dd171-129">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dd171-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

