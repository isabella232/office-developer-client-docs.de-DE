---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e7f652e7426792d8b4c878b7f6738439aec65348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793304"
---
# <a name="openimsgsession"></a><span data-ttu-id="67732-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="67732-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="67732-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67732-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67732-105">Erstellt und öffnet eine Sofortnachrichtensitzung, die darin enthaltenen erstellten Nachrichten gruppiert.</span><span class="sxs-lookup"><span data-stu-id="67732-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67732-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="67732-106">Header file:</span></span>  <br/> |<span data-ttu-id="67732-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="67732-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="67732-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="67732-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="67732-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="67732-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="67732-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="67732-110">Called by:</span></span>  <br/> |<span data-ttu-id="67732-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="67732-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="67732-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="67732-112">Parameters</span></span>

 <span data-ttu-id="67732-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="67732-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="67732-114">[in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="67732-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="67732-115">MAPI muss diese Zuordnungsmethode verwenden, bei der Arbeit mit der OLE- [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="67732-115">MAPI needs to use this allocation method when working with the OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) interface.</span></span> 
    
 <span data-ttu-id="67732-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="67732-116">_ulFlags_</span></span>
  
> <span data-ttu-id="67732-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="67732-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="67732-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="67732-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="67732-119">[out] Zeiger auf einen Zeiger auf das zurückgegebene Nachricht Session-Objekt.</span><span class="sxs-lookup"><span data-stu-id="67732-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67732-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="67732-120">Return value</span></span>

<span data-ttu-id="67732-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="67732-121">S_OK</span></span>
  
> <span data-ttu-id="67732-122">Die Sitzung geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="67732-122">The session was opened.</span></span>
    
<span data-ttu-id="67732-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="67732-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="67732-124">_LpMalloc_ oder _LppMsgSess_ ist NULL.</span><span class="sxs-lookup"><span data-stu-id="67732-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="67732-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="67732-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="67732-126">Es wurden ungültige Flags übergeben.</span><span class="sxs-lookup"><span data-stu-id="67732-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="67732-127">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67732-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="67732-128">Beim Aufruf von dieser Funktion wird ein Client oder Dienstanbieter die Option MAPI_UNICODE Unicode MSG-Dateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67732-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="67732-129">Die resultierende [Imessage](imessageimapiprop.md) Datei zeigt STORE_UNICODE_OK in seiner PR_STORE_SUPPORT_MASK und Unicode-Eigenschaften unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67732-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="67732-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67732-130">Remarks</span></span>

<span data-ttu-id="67732-131">Eine Sofortnachrichtensitzung wird von Clientanwendungen und Dienstanbieter, die für den Umgang mit mehreren möchten verwandte MAPI [IMessage: IMAPIProp](imessageimapiprop.md) Objekte auf der Basis zugrunde liegenden OLE **IStorage** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="67732-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="67732-132">Der Client oder Anbieter verwendet die Funktionen **OpenIMsgSession** und [CloseIMsgSession](closeimsgsession.md) um die Erstellung solcher Nachrichten innerhalb einer Sofortnachrichtensitzung zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="67732-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="67732-133">Sobald die Nachricht Sitzung geöffnet ist, übergibt der Client oder der Anbieter einen Zeiger auf es in einem Aufruf von [OpenIMsgOnIStg](openimsgonistg.md) zum Erstellen einer neuen **IMessage**- auf - **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="67732-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="67732-134">Eine Sofortnachrichtensitzung werden von nachverfolgt alle **IMessage**- auf - **IStorage** -Objekten, die während der Dauer der Sitzung, zusätzlich zu aller Anlagen und andere Eigenschaften der Nachrichten erstellt.</span><span class="sxs-lookup"><span data-stu-id="67732-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="67732-135">Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, wird dieser Objekte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="67732-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="67732-136">**CloseIMsgSession** aufrufen, ist die einzige Möglichkeit **IMessage**- auf - **IStorage** -Objekte zu schließen.</span><span class="sxs-lookup"><span data-stu-id="67732-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="67732-137">**OpenIMsgSession** wird von Clients und Anbietern, die die Möglichkeit, mehrere verwandte Nachrichten als OLE- **IStorage** Objekte behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="67732-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="67732-138">Wenn nur eine dieser Nachrichten gleichzeitig geöffnet sein, besteht es keine Notwendigkeit zum Nachverfolgen von mehrere Nachrichten und keinen Grund eine Sofortnachrichtensitzung mit **OpenIMsgSession**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67732-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="67732-139">Da Umgang mit einem zugrunde liegenden OLE-Objekt muss MAPI OLE Zuweisung von virtuellem Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="67732-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="67732-140">Weitere Informationen zu OLE strukturierte Speicherobjekte und OLE-arbeitsspeicherreservierung, finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="67732-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

