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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792176"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="c4945-103">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4945-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="c4945-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4945-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4945-105">Ermöglicht das Formular Viewer Formular anzeigen Kontexten und Formular-Benachrichtigung zum Formular Verben ausführen und Herunterfahren Formulare entwickelt.</span><span class="sxs-lookup"><span data-stu-id="c4945-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4945-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c4945-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4945-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c4945-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="c4945-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="c4945-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c4945-109">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="c4945-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="c4945-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c4945-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4945-111">Formular-Servern</span><span class="sxs-lookup"><span data-stu-id="c4945-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="c4945-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c4945-112">Called by:</span></span>  <br/> |<span data-ttu-id="c4945-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="c4945-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="c4945-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c4945-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c4945-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="c4945-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="c4945-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="c4945-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c4945-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="c4945-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c4945-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c4945-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c4945-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="c4945-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="c4945-120">Stellt ein Ansichtskontext für das Formular her.</span><span class="sxs-lookup"><span data-stu-id="c4945-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="c4945-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="c4945-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="c4945-122">Gibt den aktuellen Ansichtskontext für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="c4945-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="c4945-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="c4945-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="c4945-124">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="c4945-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="c4945-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="c4945-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="c4945-126">Fordert, dass das Formular ausführen, was es Aufgaben ein bestimmtes Verb zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c4945-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="c4945-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="c4945-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="c4945-128">Registriert einen Formular-Viewer für Benachrichtigungen über Ereignisse, die Einfluss auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="c4945-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="c4945-129">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4945-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="c4945-130">Eine Registrierung für Benachrichtigungen mit einem Formular Viewer zuvor durch Aufrufen der **Advise**hergestellt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c4945-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="c4945-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="c4945-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="c4945-132">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, der das Form-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c4945-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4945-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4945-133">See also</span></span>



[<span data-ttu-id="c4945-134">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c4945-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

