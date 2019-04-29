---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412863"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="18ab6-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18ab6-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="18ab6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ab6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18ab6-105">Ermöglicht den Zugriff auf einen Nachrichtenspeicher Anbieter über ein Objekt des Nachrichtenspeicher Anbieters.</span><span class="sxs-lookup"><span data-stu-id="18ab6-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="18ab6-106">Dieses Objekt des Nachrichtenspeicher Anbieters wird bei der Anbieter Anmeldung von der [MSProviderInit](msproviderinit.md) -Einstiegspunktfunktion des Nachrichtenspeicher Anbieters zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18ab6-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="18ab6-107">Das Nachrichtenspeicher-Anbieterobjekt wird hauptsächlich von Clientanwendungen und dem MAPI-Spooler zum Öffnen von Nachrichten speichern verwendet.</span><span class="sxs-lookup"><span data-stu-id="18ab6-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18ab6-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="18ab6-108">Header file:</span></span>  <br/> |<span data-ttu-id="18ab6-109">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="18ab6-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="18ab6-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="18ab6-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="18ab6-111">Nachrichtenspeicheranbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="18ab6-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="18ab6-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="18ab6-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="18ab6-113">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="18ab6-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="18ab6-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="18ab6-114">Called by:</span></span>  <br/> |<span data-ttu-id="18ab6-115">MAPI und der MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="18ab6-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="18ab6-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="18ab6-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="18ab6-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="18ab6-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="18ab6-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="18ab6-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="18ab6-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="18ab6-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="18ab6-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="18ab6-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="18ab6-121">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="18ab6-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="18ab6-122">Schließt einen Nachrichtenspeicher Anbieter ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="18ab6-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="18ab6-123">Logon</span><span class="sxs-lookup"><span data-stu-id="18ab6-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="18ab6-124">Protokolliert MAPI für eine Instanz eines Nachrichtenspeicher Anbieters.</span><span class="sxs-lookup"><span data-stu-id="18ab6-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="18ab6-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="18ab6-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="18ab6-126">Protokolliert den MAPI-Spooler in einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="18ab6-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="18ab6-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="18ab6-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="18ab6-128">Vergleicht zwei Nachrichtenspeicher Eintrags-IDs, um zu bestimmen, ob Sie auf dasselbe Store-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="18ab6-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18ab6-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18ab6-129">Remarks</span></span>

<span data-ttu-id="18ab6-130">MAPI verwendet ein Nachrichtenspeicher-Anbieterobjekt pro Sitzung, unabhängig davon, wie viele Nachrichtenspeicher vom Informationsspeicher Anbieter geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="18ab6-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="18ab6-131">Wenn sich eine zweite MAPI-Sitzung bei einem geöffneten Speicher anmeldet, ruft MAPI **MSProviderInit** ein zweites Mal auf, um ein neues Nachrichtenspeicher-Anbieterobjekt für die zu verwendende Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="18ab6-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="18ab6-132">Ein Nachrichtenspeicher-Anbieterobjekt muss Folgendes enthalten, damit es ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="18ab6-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="18ab6-133">Ein _lpMalloc_ -Routine Zeiger zur Speicherzuweisung für die Verwendung durch alle Speicher, die mithilfe dieses Anbieterobjekts geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="18ab6-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="18ab6-134">Die _lpfAllocateBuffer_-, _ lpfAllocateMore _-und _lpfFreeBuffer_ -Routine Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md)-, [MAPIAllocateMore](mapiallocatemore.md)-und [mapifreebufferfreigegeben](mapifreebuffer.md) -Speicher Zuordnungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="18ab6-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="18ab6-135">Eine verknüpfte Liste aller Speicher, die mithilfe dieses Anbieterobjekts geöffnet und noch nicht geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="18ab6-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18ab6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ab6-136">See also</span></span>



[<span data-ttu-id="18ab6-137">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="18ab6-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

