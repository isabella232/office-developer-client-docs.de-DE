---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436384"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="6246f-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6246f-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="6246f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6246f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6246f-105">Ermöglicht es den Formular Viewern, mit Formular Ansichts Kontexten und Formular Benachrichtigungen zu arbeiten, Formular Verben auszuführen und Formulare herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="6246f-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6246f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6246f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6246f-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="6246f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6246f-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="6246f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6246f-109">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="6246f-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="6246f-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6246f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6246f-111">Formularserver</span><span class="sxs-lookup"><span data-stu-id="6246f-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="6246f-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6246f-112">Called by:</span></span>  <br/> |<span data-ttu-id="6246f-113">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="6246f-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="6246f-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6246f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6246f-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="6246f-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="6246f-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="6246f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6246f-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="6246f-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6246f-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6246f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6246f-119">SetViewcontext</span><span class="sxs-lookup"><span data-stu-id="6246f-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="6246f-120">Richtet einen Ansichtskontext für das Formular ein.</span><span class="sxs-lookup"><span data-stu-id="6246f-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="6246f-121">GetViewcontext</span><span class="sxs-lookup"><span data-stu-id="6246f-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="6246f-122">Gibt den aktuellen Ansichtskontext für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="6246f-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="6246f-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="6246f-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="6246f-124">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="6246f-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="6246f-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="6246f-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="6246f-126">Fordert, dass das Formular alle Aufgaben ausführt, die es einem bestimmten Verb zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6246f-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="6246f-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="6246f-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="6246f-128">Registriert einen Formular-Viewer für Benachrichtigungen zu Ereignissen, die das Formular betreffen.</span><span class="sxs-lookup"><span data-stu-id="6246f-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="6246f-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="6246f-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="6246f-130">Bricht eine Registrierung für Benachrichtigungen mit einem Formular Betrachter ab, der zuvor durch Aufrufen von **Advise**eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="6246f-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="6246f-131">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="6246f-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="6246f-132">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Form-Objekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="6246f-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6246f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6246f-133">See also</span></span>



[<span data-ttu-id="6246f-134">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6246f-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

