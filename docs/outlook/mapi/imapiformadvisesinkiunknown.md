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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286604"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="8027a-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8027a-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="8027a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8027a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8027a-105">Ermöglicht Formular Servern das Empfangen von Benachrichtigungen von Formular Viewern.</span><span class="sxs-lookup"><span data-stu-id="8027a-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8027a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8027a-106">Header file:</span></span>  <br/> |<span data-ttu-id="8027a-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="8027a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8027a-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="8027a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8027a-109">Form Advise Sink-Objekte</span><span class="sxs-lookup"><span data-stu-id="8027a-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="8027a-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8027a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8027a-111">Formularserver</span><span class="sxs-lookup"><span data-stu-id="8027a-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="8027a-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8027a-112">Called by:</span></span>  <br/> |<span data-ttu-id="8027a-113">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="8027a-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="8027a-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8027a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8027a-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8027a-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="8027a-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="8027a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8027a-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="8027a-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8027a-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8027a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8027a-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="8027a-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="8027a-120">Gibt an, dass eine Änderung im Status des Formular-Viewers aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8027a-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="8027a-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="8027a-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="8027a-122">Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigende Nachricht behandeln kann.</span><span class="sxs-lookup"><span data-stu-id="8027a-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8027a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8027a-123">Remarks</span></span>

<span data-ttu-id="8027a-124">Formularserver verwenden ein Advise-Senke-Objekt, um **IMAPIFormAdviseSink** zu implementieren, anstatt Sie mit Ihrem Form-Objekt einzubinden.</span><span class="sxs-lookup"><span data-stu-id="8027a-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="8027a-125">Daher sollten Formular Betrachter einen fehlgeschlagenen Aufruf der [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode eines Formulars erwarten, um einen Zeiger auf diese Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8027a-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="8027a-126">Formularserver rufen die [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode eines Viewers auf, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8027a-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="8027a-127">Ein Zeiger auf Ihre **IMAPIFormAdviseSink** -Implementierung ist als Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="8027a-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8027a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8027a-128">See also</span></span>



[<span data-ttu-id="8027a-129">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8027a-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

