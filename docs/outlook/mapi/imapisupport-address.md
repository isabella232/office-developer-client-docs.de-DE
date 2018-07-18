---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792345"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="d5227-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="d5227-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="d5227-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5227-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5227-105">Zeigt das Dialogfeld allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="d5227-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="d5227-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5227-106">Parameters</span></span>

 <span data-ttu-id="d5227-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d5227-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d5227-108">[in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="d5227-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="d5227-109">Bei der Eingabe muss immer ein Fensterhandle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5227-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="d5227-110">Wenn das Flag DIALOG_SDI in der [ADRPARM](adrparm.md) -Struktur, die auf das durch den Parameter _LpAdrParms_ festgelegt ist, wird bei der Ausgabe der Fensterhandle des modalen Dialogfelds zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5227-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="d5227-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="d5227-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="d5227-112">[in, out] Ein Zeiger auf eine **ADRPARM** -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert.</span><span class="sxs-lookup"><span data-stu-id="d5227-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="d5227-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="d5227-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="d5227-114">[in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste.</span><span class="sxs-lookup"><span data-stu-id="d5227-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="d5227-115">Bei der Eingabe diese Liste ist entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn die Liste nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d5227-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="d5227-116">Ausgabe _LppAdrList_ zeigt auf eine aktualisierte Liste der Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d5227-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5227-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d5227-117">Return value</span></span>

<span data-ttu-id="d5227-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5227-118">S_OK</span></span> 
  
> <span data-ttu-id="d5227-119">Das Dialogfeld Adresse wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5227-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5227-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5227-120">Remarks</span></span>

<span data-ttu-id="d5227-121">Die **IMAPISupport::Address** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5227-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="d5227-122">Von adressbuchanbietern implementierte Aufrufen **Adresse** zum Erstellen oder aktualisieren eine Liste der Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d5227-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="d5227-123">Jeden Empfänger wird in eine Struktur [ADRENTRY](adrentry.md) beschrieben, die in der [ADRLIST](adrlist.md) -Struktur, die auf das durch den Parameter _LppAdrList_ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d5227-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="d5227-124">Die **ADRENTRY** -Datenstruktur enthält ein Array von Eigenschaftswerten Empfänger, von denen des Empfängers Typ oder **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="d5227-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="d5227-125">Diese Struktur **ADRLIST** kann an einen Client für die Verwendung als _LpMods_ -Parameter in einem Aufruf von [IMessage::ModifyRecipients](imessage-modifyrecipients.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5227-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="d5227-126">Jeden Empfänger in der Struktur **ADRLIST** kann entweder aufgelöst werden gibt an, dass eine Eigenschaftswerte dessen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft ist oder nicht aufgelöst ist, gibt an, dass die Eigenschaft **PR_ENTRYID** ist, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d5227-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="d5227-127">Zusätzlich zur **PR_ENTRYID**gehören aufgelösten Empfänger die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d5227-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="d5227-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="d5227-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="d5227-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d5227-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d5227-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d5227-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d5227-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d5227-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="d5227-132">Nicht aufgelösten Empfänger beinhalten in der Regel nur **PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="d5227-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5227-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d5227-133">Notes to callers</span></span>

<span data-ttu-id="d5227-134">Die **ADRLIST** -Struktur, der der Anrufer übergibt möglicherweise eine andere Größe aus der Struktur, die MAPI zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d5227-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="d5227-135">Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, weisen Sie des Speichers separat für jedes [SPropValue](spropvalue.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d5227-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="d5227-136">Verwenden Sie die Verweise auf die MAPI-Speicherverwaltungsfunktionen zu Ihrer [ABProviderInit](abproviderinit.md) -Funktion übergebene Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d5227-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="d5227-137">Reservieren Sie Speicher mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) für **ADRLIST** und jede Eigenschaft Wert Struktur in den **ADRENTRY** Strukturen in **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="d5227-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="d5227-138">Wenn **Adresse** eine größere **ADRLIST** Struktur zurückgeben muss, oder wenn Sie NULL für _LppAdrList_übergeben haben, **Adresse** Originalstruktur frei und ordnet einen neuen Anwendungspool.</span><span class="sxs-lookup"><span data-stu-id="d5227-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="d5227-139">**Adresse** auch zusätzliche Eigenschaft Wert Strukturen in der Struktur **ADRLIST** reserviert und alten entsprechend frei.</span><span class="sxs-lookup"><span data-stu-id="d5227-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="d5227-140">Weitere Informationen zur Verwaltung des Arbeitsspeichers für **ADRLIST** Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="d5227-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="d5227-141">**Adresse** zurückgegeben sofort, wenn das Flag DIALOG_SDI in der Struktur **ADRPARM** im _LpAdrParms_ -Parameter festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5227-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5227-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5227-142">See also</span></span>



[<span data-ttu-id="d5227-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d5227-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="d5227-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="d5227-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="d5227-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d5227-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="d5227-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="d5227-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="d5227-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="d5227-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="d5227-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="d5227-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="d5227-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="d5227-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="d5227-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d5227-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="d5227-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="d5227-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="d5227-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d5227-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d5227-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d5227-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="d5227-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d5227-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d5227-155">PidTagAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d5227-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="d5227-156">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d5227-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="d5227-157">PidTagDisplayType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d5227-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="d5227-158">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d5227-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="d5227-159">PidTagRecipientType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d5227-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="d5227-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d5227-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="d5227-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="d5227-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="d5227-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5227-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="d5227-163">Verwalten von Speicher für ADRLIST- und SRowSet-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d5227-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

