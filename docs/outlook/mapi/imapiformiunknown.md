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
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587131"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="daf80-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="daf80-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="daf80-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daf80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daf80-105">Ermöglicht das Formular Viewer Formular anzeigen Kontexten und Formular-Benachrichtigung zum Formular Verben ausführen und Herunterfahren Formulare entwickelt.</span><span class="sxs-lookup"><span data-stu-id="daf80-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daf80-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="daf80-106">Header file:</span></span>  <br/> |<span data-ttu-id="daf80-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="daf80-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="daf80-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="daf80-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="daf80-109">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="daf80-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="daf80-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="daf80-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="daf80-111">Formular-Servern</span><span class="sxs-lookup"><span data-stu-id="daf80-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="daf80-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="daf80-112">Called by:</span></span>  <br/> |<span data-ttu-id="daf80-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="daf80-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="daf80-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="daf80-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="daf80-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="daf80-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="daf80-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="daf80-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="daf80-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="daf80-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="daf80-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="daf80-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="daf80-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="daf80-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="daf80-120">Stellt ein Ansichtskontext für das Formular her.</span><span class="sxs-lookup"><span data-stu-id="daf80-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="daf80-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="daf80-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="daf80-122">Gibt den aktuellen Ansichtskontext für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="daf80-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="daf80-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="daf80-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="daf80-124">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="daf80-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="daf80-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="daf80-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="daf80-126">Fordert, dass das Formular ausführen, was es Aufgaben ein bestimmtes Verb zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="daf80-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="daf80-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="daf80-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="daf80-128">Registriert einen Formular-Viewer für Benachrichtigungen über Ereignisse, die Einfluss auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="daf80-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="daf80-129">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="daf80-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="daf80-130">Eine Registrierung für Benachrichtigungen mit einem Formular Viewer zuvor durch Aufrufen der **Advise**hergestellt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="daf80-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="daf80-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="daf80-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="daf80-132">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, der das Form-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="daf80-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daf80-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="daf80-133">See also</span></span>



[<span data-ttu-id="daf80-134">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="daf80-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

