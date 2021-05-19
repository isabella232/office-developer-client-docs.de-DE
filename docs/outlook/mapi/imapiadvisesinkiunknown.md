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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409566"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="b07e1-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b07e1-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="b07e1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b07e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b07e1-105">Implementiert ein Advise Sink-Objekt für die Behandlung von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="b07e1-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="b07e1-106">Ein Zeiger auf ein Advise Sink-Objekt wird in einem Aufruf der **Advise-Methode** eines Dienstanbieters übergeben, dem Mechanismus, der zum Registrieren für Benachrichtigungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b07e1-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b07e1-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b07e1-107">Header file:</span></span>  <br/> |<span data-ttu-id="b07e1-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b07e1-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b07e1-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="b07e1-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b07e1-110">Beraten von Sinkobjekten</span><span class="sxs-lookup"><span data-stu-id="b07e1-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="b07e1-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b07e1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b07e1-112">Clientanwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="b07e1-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="b07e1-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b07e1-113">Called by:</span></span>  <br/> |<span data-ttu-id="b07e1-114">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="b07e1-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="b07e1-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b07e1-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b07e1-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b07e1-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="b07e1-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="b07e1-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b07e1-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="b07e1-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b07e1-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b07e1-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b07e1-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="b07e1-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="b07e1-121">Antwortet auf eine Benachrichtigung, indem mindestens eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b07e1-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="b07e1-122">Die ausgeführten Aufgaben hängen vom Typ des Ereignisses und dem Objekt ab, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="b07e1-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b07e1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b07e1-123">See also</span></span>



[<span data-ttu-id="b07e1-124">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b07e1-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

