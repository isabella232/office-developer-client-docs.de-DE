---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 10f8f2cf44bf1a8e00f8c2b1a76826db5fc07161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791987"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="88cd3-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="88cd3-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="88cd3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88cd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88cd3-105">Zeigt das Dialogfeld Adressbuch von Outlook-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="88cd3-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="88cd3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88cd3-106">Parameters</span></span>

 <span data-ttu-id="88cd3-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="88cd3-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="88cd3-108">[in, out] Ein Zeiger auf ein Handle für das übergeordnete Fenster des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="88cd3-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="88cd3-109">Bei der Eingabe muss immer ein Fensterhandle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="88cd3-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="88cd3-110">Wenn der **UlFlags** Member des Parameters _LpAdrParms_ auf DIALOG_SDI, festgelegt ist, wird bei der Ausgabe der Fensterhandle des modalen Dialogfelds zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88cd3-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="88cd3-111">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="88cd3-111">See Remarks.</span></span> 
    
 <span data-ttu-id="88cd3-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="88cd3-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="88cd3-113">[in, out] Ein Zeiger auf eine [ADRPARM](adrparm.md) -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert.</span><span class="sxs-lookup"><span data-stu-id="88cd3-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="88cd3-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="88cd3-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="88cd3-115">[in, out] Ein Zeiger auf einen Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die Empfängerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="88cd3-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="88cd3-116">Dieser Parameter kann bei der Eingabe NULL sein oder zeigen Sie auf einen gültigen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="88cd3-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="88cd3-117">Ausgabe zeigt dieser Parameter auf einen Zeiger auf gültige Empfängerinformationen.</span><span class="sxs-lookup"><span data-stu-id="88cd3-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="88cd3-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="88cd3-118">Return value</span></span>

<span data-ttu-id="88cd3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="88cd3-119">S_OK</span></span> 
  
> <span data-ttu-id="88cd3-120">Das Dialogfeld allgemeine Adresse wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88cd3-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88cd3-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88cd3-121">Remarks</span></span>

<span data-ttu-id="88cd3-122">Wenn der **UlFlags** Member des Parameters _LpAdrParms_ vorhersehen von die Rückgabe von den Fensterhandle des modalen Dialogfelds auf Ausgabe DIALOG_SDI festgelegt ist, wird es in Outlook ignoriert. die modale Version des Dialogfelds wird immer in Outlook nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88cd3-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="88cd3-123">Die **ADRLIST** -Struktur wird wieder von MAPI an dem Anrufer über den _LppAdrList_ -Parameter übergeben enthält ein Array von [ADRENTRY](adrentry.md) -Strukturen, eine Struktur für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="88cd3-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="88cd3-124">Wenn Sie eine ausgehende Nachricht [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode in der _LpMods_ -Parameter übergeben wird, kann die **ADRLIST** -Struktur so aktualisieren Sie die Empfängerliste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88cd3-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="88cd3-125">Jede **ADRENTRY** Struktur in der Struktur **ADRLIST** enthält null oder mehr [SPropValue](spropvalue.md) Strukturen, eine Struktur für jede Eigenschaft, die für den Empfänger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88cd3-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="88cd3-126">Wenn das Dialogfeld präsentiert von der **Adresse** -Methode verwendet wird, um einen Empfänger zu entfernen kann 0 (null) **SPropValue** Strukturen sein.</span><span class="sxs-lookup"><span data-stu-id="88cd3-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="88cd3-127">Wenn ein oder mehrere **SPropValue** Strukturen vorhanden sind, wird die entsprechende **ADRENTRY** -Struktur hinzufügen oder aktualisieren einen Empfänger verwendet.</span><span class="sxs-lookup"><span data-stu-id="88cd3-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="88cd3-128">Der Empfänger kann nicht aufgelöst werden gibt an, dass eine der Strukturen **SPropValue** des Empfängers **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft beschreibt oder nicht aufgelöst, was bedeutet, dass die **PR_ENTRYID** -Eigenschaft ist, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="88cd3-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="88cd3-129">Zusätzlich zur **PR_ENTRYID**gehören aufgelösten Empfänger die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="88cd3-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="88cd3-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88cd3-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="88cd3-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88cd3-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="88cd3-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88cd3-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="88cd3-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88cd3-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="88cd3-134">Die **ADRLIST** -Struktur, der der Anrufer übergibt möglicherweise eine andere Größe aus der Struktur, die MAPI zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="88cd3-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="88cd3-135">Wenn MAPI eine größere **ADRLIST** Struktur zurückgeben muss, Originalstruktur frei und ordnet einen neuen Anwendungspool.</span><span class="sxs-lookup"><span data-stu-id="88cd3-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="88cd3-136">Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, weisen Sie des Speichers separat für jedes **SPropValue** Struktur.</span><span class="sxs-lookup"><span data-stu-id="88cd3-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="88cd3-137">Weitere Informationen zum Zuordnen und Freigeben von **ADRLIST** -Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="88cd3-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="88cd3-138">**Adresse** wird sofort zurückgegeben, wenn das Flag DIALOG_SDI im **UlFlags** -Member der Struktur **ADRPARM** im _LpAdrParms_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="88cd3-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="88cd3-139">Das Flag DIALOG_SDI für nicht-Outlook-Clients ignoriert.</span><span class="sxs-lookup"><span data-stu-id="88cd3-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="88cd3-140">DIALOG_SDI ignoriert wird, wird die modale Version des Dialogfelds angezeigt werden und ein Zeiger auf ein Handle sollte nicht in _LpulUIParam_erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="88cd3-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="88cd3-141">**Adresse** unterstützt Unicode-Zeichenfolgen in der Struktur **ADRPARM** , wenn AB_UNICODEUI im **UlFlags** -Member **ADRPARM** im _LpAdrParms_ -Parameter angegeben wurde, und es Unicode-Zeichenfolgen in **unterstützt ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="88cd3-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="88cd3-142">Die Unicode-Zeichenfolgen werden in der multibyte-Zeichenfolge handeln Zeichenformat konvertiert, bevor sie im Dialogfeld Outlook-Adresse Adressbuch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="88cd3-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="88cd3-143">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="88cd3-143">MFCMAPI reference</span></span>

<span data-ttu-id="88cd3-144">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="88cd3-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="88cd3-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="88cd3-145">**File**</span></span>|<span data-ttu-id="88cd3-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="88cd3-146">**Function**</span></span>|<span data-ttu-id="88cd3-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="88cd3-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="88cd3-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="88cd3-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="88cd3-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="88cd3-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="88cd3-150">MFCMAPI (engl.) verwendet die **Adresse** -Methode, um die Benutzer welches Postfach zum Öffnen auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="88cd3-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88cd3-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88cd3-151">See also</span></span>



[<span data-ttu-id="88cd3-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="88cd3-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="88cd3-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="88cd3-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="88cd3-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="88cd3-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="88cd3-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="88cd3-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="88cd3-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="88cd3-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="88cd3-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="88cd3-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="88cd3-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="88cd3-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="88cd3-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="88cd3-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="88cd3-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="88cd3-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="88cd3-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="88cd3-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="88cd3-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="88cd3-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="88cd3-163">' Srowset '</span><span class="sxs-lookup"><span data-stu-id="88cd3-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="88cd3-164">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="88cd3-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="88cd3-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="88cd3-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="88cd3-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="88cd3-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

