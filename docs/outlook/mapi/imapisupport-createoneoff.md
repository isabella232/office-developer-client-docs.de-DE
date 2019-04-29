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
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="f4e80-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="f4e80-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="f4e80-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4e80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4e80-105">Erstellt eine Eintrags-ID für eine einmalige Adresse.</span><span class="sxs-lookup"><span data-stu-id="f4e80-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f4e80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4e80-106">Parameters</span></span>

 <span data-ttu-id="f4e80-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="f4e80-107">_lpszName_</span></span>
  
> <span data-ttu-id="f4e80-108">in Ein Zeiger auf den Anzeigenamen des Empfängers die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f4e80-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="f4e80-109">Der _lpszName_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f4e80-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f4e80-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="f4e80-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="f4e80-111">in Ein Zeiger auf den Adresstyp (wie FAX, SMTP oder x500) des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="f4e80-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="f4e80-112">Der _lpszAdrType_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f4e80-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="f4e80-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="f4e80-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="f4e80-114">in Ein Zeiger auf die Messaging Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="f4e80-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="f4e80-115">Der _lpszAddress_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f4e80-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="f4e80-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4e80-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f4e80-117">in Eine Bitmaske von Flags, die sich auf den einmaligen Empfänger auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f4e80-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="f4e80-118">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f4e80-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f4e80-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="f4e80-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="f4e80-120">Der Empfänger kann formatierten Nachrichteninhalt nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f4e80-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="f4e80-121">Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft des Empfängers auf false fest.</span><span class="sxs-lookup"><span data-stu-id="f4e80-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="f4e80-122">Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die Messaging Adresse des Empfängers, auf die durch _lpszAddress_ verwiesen wird, wird als Internet Adresse interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f4e80-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="f4e80-123">In diesem Fall wird **PR_SEND_RICH_INFO** auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f4e80-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="f4e80-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4e80-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f4e80-125">Der Anzeigename, der Adresstyp und die Adresse sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="f4e80-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="f4e80-126">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="f4e80-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f4e80-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4e80-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="f4e80-128">Out Ein Zeiger auf die Anzahl von Bytes in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f4e80-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f4e80-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4e80-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="f4e80-130">Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="f4e80-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4e80-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4e80-131">Return value</span></span>

<span data-ttu-id="f4e80-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4e80-132">S_OK</span></span> 
  
> <span data-ttu-id="f4e80-133">Der einmalige Eintragsbezeichner wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="f4e80-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4e80-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4e80-134">Remarks</span></span>

<span data-ttu-id="f4e80-135">Die **IMAPISupport:: CreateOneOff** -Methode wird für alle Support Objekte des Dienstanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="f4e80-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="f4e80-136">Dienstanbieter rufen **CreateOneOff** auf, um eine Eintrags-ID für einen einmaligen Empfänger (einen Empfänger, der keinem der Container von einem der derzeit geladenen Adressbuchanbieter gehört) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f4e80-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4e80-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f4e80-137">Notes to callers</span></span>

<span data-ttu-id="f4e80-138">Wenn Sie die von **CreateOneOff**zurückgegebene Eintrags-ID nicht mehr verwenden möchten, müssen Sie den für die Eintrags-ID reservierten Arbeitsspeicher mithilfe der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="f4e80-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="f4e80-139">Hinweise für Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="f4e80-139">Notes to Transport Providers</span></span>

<span data-ttu-id="f4e80-140">Unterstützen Sie das Transport Neutral Encapsulation Format (TNEF), und verwenden Sie den Wert der **PR_SEND_RICH_INFO** -Eigenschaft, um zu bestimmen, ob TNEF beim Transport einer Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4e80-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="f4e80-141">Wenn Sie TNEF nicht unterstützen oder keine Nachricht in diesem Format senden, wenn Sie angefordert wird, kann dies ein Problem für formularbasierte Clients oder Clients sein, die benutzerdefinierte MAPI-Eigenschaften erfordern.</span><span class="sxs-lookup"><span data-stu-id="f4e80-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="f4e80-142">Der Grund ist, dass TNEF in der Regel zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4e80-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4e80-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4e80-143">See also</span></span>



[<span data-ttu-id="f4e80-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f4e80-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f4e80-145">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4e80-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="f4e80-146">Kanonische Pidtagsendrichinfo (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4e80-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="f4e80-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4e80-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

