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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9444806347c97077b03922b116e2ed7f61665cc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792677"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="992bd-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="992bd-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="992bd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="992bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="992bd-105">Ermöglicht den Zugriff auf eine Nachricht-Anbieter über eine Nachricht Speicher-Anbieter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="992bd-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="992bd-106">Dieses Objekt "Message" Speicher-Anbieter wird bei der Anmeldung Anbieter von der Nachricht Informationsdienst [MSProviderInit](msproviderinit.md) Eintrag-Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="992bd-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="992bd-107">Message-Speicher-Anbieter-Objekts wird hauptsächlich von Clientanwendungen und die MAPI-Warteschlange zum Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="992bd-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="992bd-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="992bd-108">Header file:</span></span>  <br/> |<span data-ttu-id="992bd-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="992bd-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="992bd-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="992bd-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="992bd-111">Message-Speicher-Anbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="992bd-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="992bd-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="992bd-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="992bd-113">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="992bd-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="992bd-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="992bd-114">Called by:</span></span>  <br/> |<span data-ttu-id="992bd-115">MAPI- und die MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="992bd-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="992bd-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="992bd-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="992bd-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="992bd-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="992bd-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="992bd-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="992bd-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="992bd-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="992bd-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="992bd-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="992bd-121">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="992bd-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="992bd-122">Schließt einen Anbieter für Nachricht Anmelden in einer bestimmten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="992bd-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="992bd-123">Logon</span><span class="sxs-lookup"><span data-stu-id="992bd-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="992bd-124">Protokolle MAPI an eine Instanz der Anbieter eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="992bd-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="992bd-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="992bd-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="992bd-126">Die MAPI-Warteschlange an einen Nachrichtenspeicher protokolliert.</span><span class="sxs-lookup"><span data-stu-id="992bd-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="992bd-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="992bd-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="992bd-128">Vergleicht zwei e-Mail-Store-Eintragsbezeichner, um zu bestimmen, ob sie auf das gleiche Store-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="992bd-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="992bd-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="992bd-129">Remarks</span></span>

<span data-ttu-id="992bd-130">MAPI verwendet einen Speicher-Anbieterobjekt "Message" pro Sitzung, unabhängig davon, wie viele Nachricht Speicher Speicheranbieter geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="992bd-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="992bd-131">Wenn eine zweite MAPI-Sitzung anmeldet alle geöffneten Informationsspeicher, ruft MAPI zum Erstellen eines neuen Nachricht Speicher-Anbieter-Objekts für diese Sitzung verwendet ein zweites Mal an **MSProviderInit** .</span><span class="sxs-lookup"><span data-stu-id="992bd-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="992bd-132">Ein Objekt "Message" Speicher-Anbieter muss die folgenden ordnungsgemäß funktioniert enthalten:</span><span class="sxs-lookup"><span data-stu-id="992bd-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="992bd-133">Ein _LpMalloc_ -Zuweisung von virtuellem Speicher routinemäßige Zeiger für die Verwendung durch alle Speicher, die mit diesem Anbieterobjekt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="992bd-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="992bd-134">Die _LpfAllocateBuffer_, _ LpfAllocateMore _ und _LpfFreeBuffer_ routinemäßige Zeiger auf die Speicherverwaltungsfunktionen [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="992bd-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="992bd-135">Eine verknüpfte Liste aller Geschäfte mit diesem Anbieterobjekt geöffnet und noch nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="992bd-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="992bd-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="992bd-136">See also</span></span>



[<span data-ttu-id="992bd-137">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="992bd-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

