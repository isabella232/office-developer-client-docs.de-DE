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
ms.openlocfilehash: 1cfd4afbda5892e96a1d74ca56f4a6d1f98e2268
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792343"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="1f58a-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1f58a-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="1f58a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f58a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f58a-105">Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.</span><span class="sxs-lookup"><span data-stu-id="1f58a-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1f58a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f58a-106">Parameters</span></span>

 <span data-ttu-id="1f58a-107">_Wert_</span><span class="sxs-lookup"><span data-stu-id="1f58a-107">_lpszName_</span></span>
  
> <span data-ttu-id="1f58a-108">[in] Ein Zeiger auf den Anzeigenamen des Empfängers die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1f58a-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="1f58a-109">Der _Wert_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1f58a-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="1f58a-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="1f58a-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="1f58a-111">[in] Ein Zeiger auf den Adresstyp (wie FAX, SMTP oder X500) des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1f58a-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="1f58a-112">Der Parameter _LpszAdrType_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1f58a-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1f58a-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="1f58a-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="1f58a-114">[in] Ein Zeiger auf die messaging-Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1f58a-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="1f58a-115">Der Parameter _LpszAddress_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1f58a-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1f58a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f58a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1f58a-117">[in] Eine Bitmaske aus Flags, die den einmal-Empfänger auswirkt.</span><span class="sxs-lookup"><span data-stu-id="1f58a-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="1f58a-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1f58a-118">The following flags can be set:</span></span>
    
<span data-ttu-id="1f58a-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="1f58a-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="1f58a-120">Der Empfänger kann nicht formatierte Nachrichteninhalt behandeln.</span><span class="sxs-lookup"><span data-stu-id="1f58a-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="1f58a-121">Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, wird der MAPI-Eigenschaft des Empfängers- **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f58a-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="1f58a-122">Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, wird diese Eigenschaft von MAPI auf TRUE festgelegt, es sei denn, die Adresse des Empfängers messaging auf das _LpszAddress_ interpretiert wird, um eine IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="1f58a-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="1f58a-123">In diesem Fall wird MAPI **PR_SEND_RICH_INFO** auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f58a-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="1f58a-124">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f58a-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1f58a-125">Der Anzeigename, Adresstyp und Adresse sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="1f58a-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="1f58a-126">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="1f58a-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1f58a-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1f58a-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="1f58a-128">[out] Ein Zeiger auf die Anzahl von Bytes in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="1f58a-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1f58a-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="1f58a-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="1f58a-130">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="1f58a-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f58a-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f58a-131">Return value</span></span>

<span data-ttu-id="1f58a-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f58a-132">S_OK</span></span> 
  
> <span data-ttu-id="1f58a-133">Der Bezeichner des Eingangs wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f58a-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f58a-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f58a-134">Remarks</span></span>

<span data-ttu-id="1f58a-135">Die **IMAPISupport::CreateOneOff** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="1f58a-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="1f58a-136">Dienstanbieter anrufen **CreateOneOff** zum Erstellen eines Eintrags-ID für einen einmaligen Empfänger (Empfänger, die nicht zu keiner der Container aus der aktuell geladenen adressbuchanbietern implementierte gehört).</span><span class="sxs-lookup"><span data-stu-id="1f58a-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1f58a-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1f58a-137">Notes to callers</span></span>

<span data-ttu-id="1f58a-138">Wenn Sie die Eintrags-ID von **CreateOneOff**zurückgegeben werden, frei Arbeitsspeichers für die Eintrags-ID mithilfe der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1f58a-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="1f58a-139">Hinweise für Transport-Anbieter</span><span class="sxs-lookup"><span data-stu-id="1f58a-139">Notes to Transport Providers</span></span>

<span data-ttu-id="1f58a-140">Unterstützen Sie der Transport Neutral Encapsulation Format (TNEF), und verwenden Sie den Wert der Eigenschaft **PR_SEND_RICH_INFO** um zu ermitteln, ob TNEF verwenden, wenn Sie eine Nachricht transport.</span><span class="sxs-lookup"><span data-stu-id="1f58a-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="1f58a-141">TNEF nicht unterstützt, oder Senden einer Nachricht nicht in diesem Format aus, wenn sie dazu aufgefordert werden möglicherweise ein Problem für formularbasierte oder Clients, die eine benutzerdefinierte MAPI-Eigenschaften erfordern.</span><span class="sxs-lookup"><span data-stu-id="1f58a-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="1f58a-142">Dies ist, da TNEF in der Regel zum Senden von benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f58a-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f58a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f58a-143">See also</span></span>



[<span data-ttu-id="1f58a-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1f58a-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1f58a-145">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f58a-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="1f58a-146">PidTagSendRichInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f58a-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="1f58a-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f58a-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

