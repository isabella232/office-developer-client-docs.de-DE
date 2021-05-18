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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326194"
---
# <a name="openimsgsession"></a><span data-ttu-id="31db1-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="31db1-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="31db1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31db1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31db1-105">Erstellt und öffnet eine Nachrichtensitzung, die die in ihr erstellten Nachrichten gruppen.</span><span class="sxs-lookup"><span data-stu-id="31db1-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31db1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="31db1-106">Header file:</span></span>  <br/> |<span data-ttu-id="31db1-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="31db1-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="31db1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="31db1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31db1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31db1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31db1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="31db1-110">Called by:</span></span>  <br/> |<span data-ttu-id="31db1-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="31db1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="31db1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="31db1-112">Parameters</span></span>

 <span data-ttu-id="31db1-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="31db1-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="31db1-114">[in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE [IMalloc-Schnittstelle verfügbar](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) machen soll.</span><span class="sxs-lookup"><span data-stu-id="31db1-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="31db1-115">MAPI muss diese Zuordnungsmethode verwenden, wenn sie mit der OLE [IStorage-Schnittstelle](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) arbeitet.</span><span class="sxs-lookup"><span data-stu-id="31db1-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="31db1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31db1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="31db1-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="31db1-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="31db1-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="31db1-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="31db1-119">[out] Zeiger auf einen Zeiger auf das zurückgegebene Nachrichtensitzungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="31db1-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31db1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31db1-120">Return value</span></span>

<span data-ttu-id="31db1-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="31db1-121">S_OK</span></span>
  
> <span data-ttu-id="31db1-122">Die Sitzung wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="31db1-122">The session was opened.</span></span>
    
<span data-ttu-id="31db1-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="31db1-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="31db1-124">_lpMalloc_ oder  _lppMsgSess_ ist NULL.</span><span class="sxs-lookup"><span data-stu-id="31db1-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="31db1-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="31db1-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="31db1-126">Ungültige Flags wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="31db1-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="31db1-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="31db1-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="31db1-128">Beim Aufrufen dieser Funktion legt ein Client oder Dienstanbieter das MAPI_UNICODE fest, um Unicode-MSG-Dateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="31db1-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="31db1-129">Die resultierende [Imessage-Datei](imessageimapiprop.md) STORE_UNICODE_OK in ihrer PR_STORE_SUPPORT_MASK und unterstützt Unicode-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31db1-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31db1-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31db1-130">Remarks</span></span>

<span data-ttu-id="31db1-131">Eine Nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die sich mit mehreren verwandten MAPI [IMessage : IMAPIProp-Objekten](imessageimapiprop.md) befassen möchten, die auf zugrunde liegenden OLE **IStorage-Objekten** basieren.</span><span class="sxs-lookup"><span data-stu-id="31db1-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="31db1-132">Der Client oder Anbieter verwendet die **Funktionen OpenIMsgSession** und [CloseIMsgSession,](closeimsgsession.md) um die Erstellung solcher Nachrichten in einer Nachrichtensitzung zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="31db1-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="31db1-133">Nachdem die Nachrichtensitzung geöffnet wurde, übergibt der Client oder Anbieter einen Zeiger an [openIMsgOnIStg,](openimsgonistg.md) um ein neues **IMessage**-on-IStorage-Objekt zu erstellen. </span><span class="sxs-lookup"><span data-stu-id="31db1-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="31db1-134">Eine Nachrichtensitzung verfolgt alle **IMessage** **-on-IStorage-Objekte,** die während der Sitzung erstellt wurden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="31db1-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="31db1-135">Wenn ein Client oder Anbieter **CloseIMsgSession aufruft,** werden alle diese Objekte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="31db1-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="31db1-136">Das **Aufrufen von CloseIMsgSession** ist die einzige Möglichkeit, **IMessage**-on-IStorage-Objekte **zu** schließen.</span><span class="sxs-lookup"><span data-stu-id="31db1-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="31db1-137">**OpenIMsgSession** wird von Clients und Anbietern verwendet, die die Möglichkeit benötigen, mehrere verwandte Nachrichten als OLE **IStorage-Objekte zu** behandeln.</span><span class="sxs-lookup"><span data-stu-id="31db1-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="31db1-138">Wenn nur eine solche Nachricht gleichzeitig geöffnet werden soll, müssen sie nicht mehrere Nachrichten nachverfolgen und es gibt keinen Grund, eine Nachrichtensitzung mit **OpenIMsgSession zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="31db1-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="31db1-139">Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI die OLE-Speicherzuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="31db1-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="31db1-140">Weitere Informationen zu strukturierten OLE-Speicherobjekten und der OLE-Speicherzuweisung finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="31db1-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

