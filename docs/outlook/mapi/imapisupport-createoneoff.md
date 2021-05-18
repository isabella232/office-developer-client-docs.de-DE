---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411995"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="6abe0-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="6abe0-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="6abe0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6abe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6abe0-105">Erstellt einen Eintragsbezeichner für eine eindeutige Adresse.</span><span class="sxs-lookup"><span data-stu-id="6abe0-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="6abe0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6abe0-106">Parameters</span></span>

 <span data-ttu-id="6abe0-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="6abe0-107">_lpszName_</span></span>
  
> <span data-ttu-id="6abe0-108">[in] Ein Zeiger auf den Anzeigenamen des Empfängers, **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6abe0-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="6abe0-109">Der  _lpszName-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6abe0-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="6abe0-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="6abe0-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="6abe0-111">[in] Ein Zeiger auf den Adresstyp (z. B. FAX, SMTP oder X500) des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="6abe0-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="6abe0-112">Der  _lpszAdrType-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6abe0-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="6abe0-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="6abe0-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="6abe0-114">[in] Ein Zeiger auf die Messagingadresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="6abe0-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="6abe0-115">Der  _lpszAddress-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6abe0-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="6abe0-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6abe0-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6abe0-117">[in] Eine Bitmaske mit Flags, die sich auf den einmalen Empfänger auswirkt.</span><span class="sxs-lookup"><span data-stu-id="6abe0-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="6abe0-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6abe0-118">The following flags can be set:</span></span>
    
<span data-ttu-id="6abe0-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="6abe0-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="6abe0-120">Der Empfänger kann formatierte Nachrichteninhalte nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6abe0-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="6abe0-121">Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **Eigenschaft PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) des Empfängers auf FALSE fest.</span><span class="sxs-lookup"><span data-stu-id="6abe0-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="6abe0-122">Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die von  _lpszAddress_ angezeigte Messagingadresse des Empfängers wird als Internetadresse interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6abe0-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="6abe0-123">In diesem Fall legt MAPI **PR_SEND_RICH_INFO** FALSE fest.</span><span class="sxs-lookup"><span data-stu-id="6abe0-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="6abe0-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6abe0-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6abe0-125">Anzeigename, Adresstyp und Adresse befinden sich im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6abe0-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="6abe0-126">Wenn das MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6abe0-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6abe0-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6abe0-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="6abe0-128">[out] Ein Zeiger auf die Anzahl der Bytes in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="6abe0-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6abe0-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="6abe0-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="6abe0-130">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmal verwendeten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="6abe0-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6abe0-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6abe0-131">Return value</span></span>

<span data-ttu-id="6abe0-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="6abe0-132">S_OK</span></span> 
  
> <span data-ttu-id="6abe0-133">Der eindeutige Eintragsbezeichner wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="6abe0-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6abe0-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6abe0-134">Remarks</span></span>

<span data-ttu-id="6abe0-135">Die **IMAPISupport::CreateOneOff-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="6abe0-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="6abe0-136">Dienstanbieter rufen **CreateOneOff auf,** um eine Eintrags-ID für einen einzigen Empfänger (einen Empfänger, der keinem der Container von einem der derzeit geladenen Adressbuchanbieter angehört) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6abe0-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6abe0-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6abe0-137">Notes to callers</span></span>

<span data-ttu-id="6abe0-138">Wenn Sie mit der von **CreateOneOff** zurückgegebenen Eintrags-ID fertig sind, wird der für die Eintrags-ID zugewiesene Arbeitsspeicher mithilfe der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) frei.</span><span class="sxs-lookup"><span data-stu-id="6abe0-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="6abe0-139">Hinweise zu Transportanbietern</span><span class="sxs-lookup"><span data-stu-id="6abe0-139">Notes to Transport Providers</span></span>

<span data-ttu-id="6abe0-140">Unterstützen Sie das Transport Neutral Encapsulation Format (TNEF) und verwenden Sie den Wert der **PR_SEND_RICH_INFO-Eigenschaft,** um zu bestimmen, ob TNEF beim Transport einer Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6abe0-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="6abe0-141">Die Nicht-Unterstützung von TNEF oder das Senden einer Nachricht in diesem Format, wenn sie angefordert wird, kann ein Problem für formularbasierte Clients oder Clients sein, die benutzerdefinierte MAPI-Eigenschaften benötigen.</span><span class="sxs-lookup"><span data-stu-id="6abe0-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="6abe0-142">Dies liegt daran, dass TNEF in der Regel zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6abe0-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6abe0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6abe0-143">See also</span></span>



[<span data-ttu-id="6abe0-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6abe0-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6abe0-145">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6abe0-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="6abe0-146">PidTagSendRichInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6abe0-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="6abe0-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6abe0-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

