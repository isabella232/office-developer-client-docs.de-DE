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
# <a name="imapiform--iunknown"></a><span data-ttu-id="33672-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33672-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="33672-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33672-105">Ermöglicht Formularanzeigen das Arbeiten mit Formularansichtskontexten und Formularbenachrichtigungen, das Ausführen von Formularverben und das Herunterfahren von Formularen.</span><span class="sxs-lookup"><span data-stu-id="33672-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33672-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="33672-106">Header file:</span></span>  <br/> |<span data-ttu-id="33672-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="33672-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="33672-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="33672-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="33672-109">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="33672-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="33672-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="33672-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="33672-111">Formularserver</span><span class="sxs-lookup"><span data-stu-id="33672-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="33672-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="33672-112">Called by:</span></span>  <br/> |<span data-ttu-id="33672-113">Formularanzeigen</span><span class="sxs-lookup"><span data-stu-id="33672-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="33672-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="33672-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="33672-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="33672-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="33672-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="33672-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="33672-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="33672-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="33672-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="33672-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="33672-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="33672-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="33672-120">Richtet einen Ansichtskontext für das Formular ein.</span><span class="sxs-lookup"><span data-stu-id="33672-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="33672-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="33672-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="33672-122">Gibt den aktuellen Ansichtskontext für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="33672-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="33672-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="33672-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="33672-124">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="33672-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="33672-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="33672-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="33672-126">Fordert an, dass das Formular alle Aufgaben ausführen soll, die es einem bestimmten Verb zurrent.</span><span class="sxs-lookup"><span data-stu-id="33672-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="33672-127">Raten</span><span class="sxs-lookup"><span data-stu-id="33672-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="33672-128">Registriert eine Formularanzeige für Benachrichtigungen über Ereignisse, die sich auf das Formular auswirken.</span><span class="sxs-lookup"><span data-stu-id="33672-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="33672-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="33672-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="33672-130">Bricht eine Registrierung für Benachrichtigungen bei einer zuvor durch Aufrufen von Advise eingerichteten Formularanzeige **ab.**</span><span class="sxs-lookup"><span data-stu-id="33672-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="33672-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="33672-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="33672-132">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formularobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="33672-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33672-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33672-133">See also</span></span>



[<span data-ttu-id="33672-134">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="33672-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

