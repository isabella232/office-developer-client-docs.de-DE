---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350918"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="df904-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df904-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="df904-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df904-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df904-105">Implementiert ein Advise-Senke-Objekt zur Behandlung von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="df904-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="df904-106">Ein Zeiger auf ein Advise-Senke-Objekt wird in einem Aufruf an die **Advise** -Methode eines Dienstanbieters übergeben, den Mechanismus, der für die Registrierung der Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df904-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df904-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="df904-107">Header file:</span></span>  <br/> |<span data-ttu-id="df904-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="df904-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="df904-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="df904-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="df904-110">Advise-Objekt</span><span class="sxs-lookup"><span data-stu-id="df904-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="df904-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="df904-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="df904-112">Client Anwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="df904-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="df904-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="df904-113">Called by:</span></span>  <br/> |<span data-ttu-id="df904-114">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="df904-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="df904-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="df904-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="df904-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="df904-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="df904-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="df904-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="df904-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="df904-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="df904-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="df904-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="df904-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="df904-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="df904-121">Reagiert auf eine Benachrichtigung, indem eine oder mehrere Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="df904-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="df904-122">Die ausgeführten Aufgaben hängen vom Ereignistyp und dem Objekt ab, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="df904-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df904-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df904-123">See also</span></span>



[<span data-ttu-id="df904-124">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="df904-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

