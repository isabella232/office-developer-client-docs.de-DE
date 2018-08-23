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
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573803"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="0dce7-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0dce7-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="0dce7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dce7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dce7-105">Implementiert eine Advise-Empfängerobjekt für die Verarbeitung der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0dce7-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="0dce7-106">Ein Zeiger auf eine Advise-Empfängerobjekt wird in einem Aufruf des Dienstanbieters **Advise** -Methode verwendeten Mechanismus zum Registrieren für die Benachrichtigung übergeben.</span><span class="sxs-lookup"><span data-stu-id="0dce7-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dce7-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0dce7-107">Header file:</span></span>  <br/> |<span data-ttu-id="0dce7-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dce7-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0dce7-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="0dce7-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="0dce7-110">Beraten der Empfängerobjekten</span><span class="sxs-lookup"><span data-stu-id="0dce7-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="0dce7-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0dce7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0dce7-112">Clientanwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="0dce7-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="0dce7-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0dce7-113">Called by:</span></span>  <br/> |<span data-ttu-id="0dce7-114">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="0dce7-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="0dce7-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="0dce7-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0dce7-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0dce7-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="0dce7-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="0dce7-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="0dce7-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="0dce7-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0dce7-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0dce7-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0dce7-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="0dce7-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="0dce7-121">Antwortet auf eine Benachrichtigung durch eine oder mehrere Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dce7-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="0dce7-122">Die Aufgaben ausgeführt, abhängig von den Typ des Ereignisses und das Objekt, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="0dce7-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dce7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dce7-123">See also</span></span>



[<span data-ttu-id="0dce7-124">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0dce7-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

