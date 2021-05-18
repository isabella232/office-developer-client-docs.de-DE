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
# <a name="imsprovider--iunknown"></a><span data-ttu-id="420aa-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="420aa-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="420aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="420aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="420aa-105">Ermöglicht den Zugriff auf einen Nachrichtenspeicheranbieter über ein Objekt des Nachrichtenspeicheranbieters.</span><span class="sxs-lookup"><span data-stu-id="420aa-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="420aa-106">Dieses Objekt des Nachrichtenspeicheranbieters wird bei der Anbieteranmeldung von der [MSProviderInit-Einstiegspunktfunktion](msproviderinit.md) des Nachrichtenspeicheranbieters zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="420aa-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="420aa-107">Das Objekt des Nachrichtenspeicheranbieters wird hauptsächlich von Clientanwendungen und dem MAPI-Spooler zum Öffnen von Nachrichtenspeichern verwendet.</span><span class="sxs-lookup"><span data-stu-id="420aa-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="420aa-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="420aa-108">Header file:</span></span>  <br/> |<span data-ttu-id="420aa-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="420aa-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="420aa-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="420aa-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="420aa-111">Nachrichtenspeicheranbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="420aa-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="420aa-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="420aa-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="420aa-113">Anbieter von Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="420aa-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="420aa-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="420aa-114">Called by:</span></span>  <br/> |<span data-ttu-id="420aa-115">MAPI und der MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="420aa-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="420aa-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="420aa-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="420aa-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="420aa-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="420aa-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="420aa-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="420aa-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="420aa-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="420aa-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="420aa-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="420aa-121">Shutdown</span><span class="sxs-lookup"><span data-stu-id="420aa-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="420aa-122">Schließt einen Nachrichtenspeicheranbieter in geordneter Weise.</span><span class="sxs-lookup"><span data-stu-id="420aa-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="420aa-123">Logon</span><span class="sxs-lookup"><span data-stu-id="420aa-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="420aa-124">Protokolliert MAPI an einer Instanz eines Nachrichtenspeicheranbieters.</span><span class="sxs-lookup"><span data-stu-id="420aa-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="420aa-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="420aa-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="420aa-126">Protokolliert den MAPI-Spooler bei einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="420aa-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="420aa-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="420aa-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="420aa-128">Vergleicht zwei Nachrichtenspeichereintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Speicherobjekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="420aa-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="420aa-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="420aa-129">Remarks</span></span>

<span data-ttu-id="420aa-130">MAPI verwendet ein Nachrichtenspeicheranbieterobjekt pro Sitzung, unabhängig davon, wie viele Nachrichtenspeicher vom Speicheranbieter geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="420aa-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="420aa-131">Wenn sich eine zweite MAPI-Sitzung bei geöffneten Speichern anmeldet, ruft MAPI **MSProviderInit** ein zweites Mal auf, um ein neues Objekt des Nachrichtenspeicheranbieters zu erstellen, das für diese Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="420aa-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="420aa-132">Ein Objekt des Nachrichtenspeicheranbieters muss Folgendes enthalten, damit es ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="420aa-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="420aa-133">Ein  lpMalloc-Speicherzuweisungsroutinenzeiger zur Verwendung durch alle Speicher, die mithilfe dieses Anbieterobjekts geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="420aa-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="420aa-134">Die _Routinezeiger lpfAllocateBuffer_, _ lpfAllocateMore _, und _lpfFreeBuffer_ zeigen auf die [Speicherzuweisungsfunktionen MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="420aa-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="420aa-135">Eine verknüpfte Liste aller Mit diesem Anbieterobjekt geöffneten und noch nicht geschlossenen Speicher.</span><span class="sxs-lookup"><span data-stu-id="420aa-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="420aa-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="420aa-136">See also</span></span>



[<span data-ttu-id="420aa-137">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="420aa-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

