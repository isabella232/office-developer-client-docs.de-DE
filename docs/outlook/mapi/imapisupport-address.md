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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331605"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="166b1-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="166b1-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="166b1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="166b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="166b1-105">Zeigt das Dialogfeld Allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="166b1-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="166b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="166b1-106">Parameters</span></span>

 <span data-ttu-id="166b1-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="166b1-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="166b1-108">[in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="166b1-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="166b1-109">Bei der Eingabe muss ein Fensterhandle immer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="166b1-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="166b1-110">Wenn das DIALOG_SDI-Flag in der [ADRPARM](adrparm.md) -Struktur festgelegt ist, auf die durch den _lpAdrParms_ -Parameter verwiesen wird, wird das Fensterhandle des Dialog Felds ohne Modus zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="166b1-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="166b1-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="166b1-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="166b1-112">[in, out] Ein Zeiger auf eine **ADRPARM** -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert.</span><span class="sxs-lookup"><span data-stu-id="166b1-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="166b1-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="166b1-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="166b1-114">[in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste.</span><span class="sxs-lookup"><span data-stu-id="166b1-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="166b1-115">Bei der Eingabe ist diese Liste entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn keine solche Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="166b1-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="166b1-116">Bei der Ausgabe zeigt _lppAdrList_ auf eine aktualisierte Liste der Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="166b1-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="166b1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="166b1-117">Return value</span></span>

<span data-ttu-id="166b1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="166b1-118">S_OK</span></span> 
  
> <span data-ttu-id="166b1-119">Das Dialogfeld Adresse wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="166b1-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="166b1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="166b1-120">Remarks</span></span>

<span data-ttu-id="166b1-121">Die **IMAPISupport:: Address** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="166b1-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="166b1-122">Adressbuchanbieter rufen die **Adresse** auf, um eine Liste der Nachrichtenempfänger zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="166b1-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="166b1-123">Jeder Empfänger wird in einer [Miet](adrentry.md) Struktur beschrieben, die in der [ADRLIST](adrlist.md) -Struktur enthalten ist, auf die durch den _lppAdrList_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="166b1-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="166b1-124">Die **Miet** Struktur enthält ein Array von Empfänger Eigenschaftswerten, von denen einer der Empfängertyp oder die **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="166b1-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="166b1-125">Diese **ADRLIST** -Struktur kann an einen Client übergeben werden, der als _lpMods_ -Parameter in einem Aufruf von [IMessage:: ModifyRecipients](imessage-modifyrecipients.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="166b1-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="166b1-126">Jeder Empfänger in der **ADRLIST** -Struktur kann aufgelöst werden, was darauf hinweist, dass einer seiner Eigenschaftswerte die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft oder nicht aufgelöst ist, was darauf hinweist, dass die **PR_ENTRYID** -Eigenschaft fehlt.</span><span class="sxs-lookup"><span data-stu-id="166b1-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="166b1-127">Zusätzlich zu **PR_ENTRYID**sind aufgelöste Empfänger die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="166b1-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="166b1-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="166b1-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="166b1-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="166b1-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="166b1-130">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="166b1-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="166b1-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="166b1-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="166b1-132">Nicht aufgelöste Empfänger schließen in der Regel nur **PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE**ein.</span><span class="sxs-lookup"><span data-stu-id="166b1-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="166b1-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="166b1-133">Notes to callers</span></span>

<span data-ttu-id="166b1-134">Die **ADRLIST** -Struktur, die der Aufrufer übergibt, kann eine andere Größe als die von MAPI zurückgegebene Struktur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="166b1-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="166b1-135">Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, ordnen Sie den Speicher für jede [SPropValue](spropvalue.md) -Struktur separat zu.</span><span class="sxs-lookup"><span data-stu-id="166b1-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="166b1-136">Verwenden Sie die Zeiger auf die MAPI-Speicher Zuweisungsfunktionen, die an Ihre [ABProviderInit](abproviderinit.md) -Funktion übergeben werden, um Arbeitsspeicher zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="166b1-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="166b1-137">Reservieren Sie Arbeitsspeicher mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion für **ADRLIST** und jeder Eigenschaftswert Struktur in den **Miet** Strukturen in **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="166b1-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="166b1-138">Wenn **Address** eine größere **ADRLIST** -Struktur zurückgeben muss oder wenn Sie NULL für _lppAdrList_übergeben haben, gibt **Address** die ursprüngliche Struktur frei und ordnet eine neue an.</span><span class="sxs-lookup"><span data-stu-id="166b1-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="166b1-139">**Address** ordnet auch zusätzliche Eigenschaftswert Strukturen in der **ADRLIST** -Struktur zu und gibt alte nach Bedarf frei.</span><span class="sxs-lookup"><span data-stu-id="166b1-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="166b1-140">Weitere Informationen zur Verwaltung von Arbeitsspeicher für **ADRLIST** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="166b1-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="166b1-141">**Address** gibt sofort zurück, wenn das DIALOG_SDI-Flag in der **ADRPARM** -Struktur im _lpAdrParms_ -Parameter festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="166b1-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="166b1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="166b1-142">See also</span></span>



[<span data-ttu-id="166b1-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="166b1-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="166b1-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="166b1-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="166b1-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="166b1-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="166b1-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="166b1-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="166b1-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="166b1-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="166b1-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="166b1-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="166b1-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="166b1-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="166b1-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="166b1-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="166b1-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="166b1-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="166b1-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="166b1-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="166b1-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="166b1-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="166b1-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="166b1-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="166b1-155">Kanonische Pidtagaddresstype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="166b1-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="166b1-156">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="166b1-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="166b1-157">Kanonische PidTagDisplayType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="166b1-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="166b1-158">Kanonische PidTagEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="166b1-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="166b1-159">Kanonische Pidtagrecipienttype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="166b1-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="166b1-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="166b1-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="166b1-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="166b1-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="166b1-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="166b1-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="166b1-163">Verwalten von Speicher für ADRLIST-und SRowSet-Strukturen</span><span class="sxs-lookup"><span data-stu-id="166b1-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

