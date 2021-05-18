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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407319"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="9e900-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="9e900-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="9e900-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e900-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e900-105">Zeigt das Dialogfeld allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="9e900-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="9e900-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e900-106">Parameters</span></span>

 <span data-ttu-id="9e900-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9e900-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="9e900-108">[in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9e900-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="9e900-109">Bei der Eingabe muss immer ein Fensterhandle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e900-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="9e900-110">Wenn bei der Ausgabe das DIALOG_SDI in der [ADRPARM-Struktur](adrparm.md) festgelegt ist, auf die der  _lpAdrParms-Parameter_ verweist, wird das Fensterhandle des Dialogfelds ohne Modus zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e900-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="9e900-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="9e900-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="9e900-112">[in, out] Ein Zeiger auf eine **ADRPARM-Struktur,** die die Präsentation und das Verhalten des Adressdialogfelds steuert.</span><span class="sxs-lookup"><span data-stu-id="9e900-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="9e900-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="9e900-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="9e900-114">[in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste.</span><span class="sxs-lookup"><span data-stu-id="9e900-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="9e900-115">Bei der Eingabe ist diese Liste entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn keine solche Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e900-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="9e900-116">Bei der Ausgabe  _zeigt lppAdrList_ auf eine aktualisierte Liste von Nachrichtenempfängern.</span><span class="sxs-lookup"><span data-stu-id="9e900-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9e900-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e900-117">Return value</span></span>

<span data-ttu-id="9e900-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e900-118">S_OK</span></span> 
  
> <span data-ttu-id="9e900-119">Das Dialogfeld Adresse wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e900-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e900-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9e900-120">Remarks</span></span>

<span data-ttu-id="9e900-121">Die **IMAPISupport::Address-Methode** wird für Unterstützungsobjekte des Adressbuchanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="9e900-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="9e900-122">Adressbuchanbieter rufen **Address auf,** um eine Liste von Nachrichtenempfängern zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e900-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="9e900-123">Jeder Empfänger wird in einer [ADRENTRY-Struktur](adrentry.md) beschrieben, die in der [ADRLIST-Struktur](adrlist.md) enthalten ist, auf die der  _lppAdrList-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="9e900-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="9e900-124">Die **ADRENTRY-Struktur** enthält ein Array von Empfängereigenschaftswerten, von denen einer der Typ des Empfängers oder PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="9e900-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="9e900-125">Diese **ADRLIST-Struktur** kann an einen Client übergeben werden, der als _lpMods-Parameter_ in einem Aufruf von [IMessage::ModifyRecipients verwendet wird.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="9e900-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="9e900-126">Jeder Empfänger in der **ADRLIST-Struktur** kann entweder aufgelöst werden, was angibt, dass einer der Eigenschaftswerte seine **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft ist, oder nicht aufgelöst, was angibt, dass die **PR_ENTRYID-Eigenschaft** fehlt.</span><span class="sxs-lookup"><span data-stu-id="9e900-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="9e900-127">Zusätzlich zu **PR_ENTRYID** enthalten aufgelöste Empfänger die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9e900-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="9e900-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="9e900-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="9e900-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e900-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="9e900-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e900-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9e900-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9e900-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="9e900-132">Nicht aufgelöste Empfänger enthalten in der Regel **nur PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="9e900-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e900-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9e900-133">Notes to callers</span></span>

<span data-ttu-id="9e900-134">Die **ADRLIST-Struktur,** die der Aufrufer übergibt, kann eine andere Größe als die von MAPI zurückgegebene Struktur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9e900-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="9e900-135">Wenn Sie speicher für die **ADRLIST-Struktur zuweisen,** weisen Sie den Arbeitsspeicher für jede [SPropValue-Struktur](spropvalue.md) separat zu.</span><span class="sxs-lookup"><span data-stu-id="9e900-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="9e900-136">Verwenden Sie die Zeiger auf die AN IHRE [ABProviderInit-Funktion übergebenen](abproviderinit.md) MAPI-Speicherzuweisungsfunktionen, um Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9e900-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="9e900-137">Zuordnen von Arbeitsspeicher mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) für **ADRLIST** und jeder Eigenschaftswertstruktur in den **ADRENTRY-Strukturen** in **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="9e900-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="9e900-138">Wenn **Address** eine größere **ADRLIST-Struktur** zurückgeben muss oder Wenn Sie NULL für  _lppAdrList_ übergeben haben, gibt **Address** die ursprüngliche Struktur frei und weist eine neue zu.</span><span class="sxs-lookup"><span data-stu-id="9e900-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="9e900-139">**Address** weist außerdem zusätzliche Eigenschaftenwertstrukturen in der **ADRLIST-Struktur** zu und gibt alte Werte frei.</span><span class="sxs-lookup"><span data-stu-id="9e900-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="9e900-140">Weitere Informationen zur Verwaltung des Arbeitsspeichers für **ADRLIST-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="9e900-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="9e900-141">**Address** gibt sofort zurück, wenn DIALOG_SDI in der **ADRPARM-Struktur** im  _lpAdrParms-Parameter festgelegt_ wurde.</span><span class="sxs-lookup"><span data-stu-id="9e900-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e900-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e900-142">See also</span></span>



[<span data-ttu-id="9e900-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="9e900-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="9e900-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="9e900-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="9e900-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9e900-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9e900-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="9e900-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="9e900-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="9e900-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="9e900-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="9e900-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="9e900-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="9e900-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="9e900-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="9e900-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="9e900-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="9e900-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="9e900-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9e900-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9e900-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="9e900-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="9e900-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9e900-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9e900-155">PidTagAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9e900-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="9e900-156">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9e900-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="9e900-157">PidTagDisplayType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9e900-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="9e900-158">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9e900-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="9e900-159">PidTagRecipientType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9e900-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="9e900-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9e900-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9e900-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9e900-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="9e900-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e900-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="9e900-163">Verwalten des Arbeitsspeichers für ADRLIST- und SRowSet-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9e900-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

