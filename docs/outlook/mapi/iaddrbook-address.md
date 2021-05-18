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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407907"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="1ce57-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="1ce57-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="1ce57-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ce57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ce57-105">Zeigt das Dialogfeld Outlook-Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="1ce57-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="1ce57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ce57-106">Parameters</span></span>

 <span data-ttu-id="1ce57-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1ce57-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="1ce57-108">[in, out] Ein Zeiger auf ein Handle des übergeordneten Fensters des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="1ce57-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="1ce57-109">Bei der Eingabe muss immer ein Fensterhandle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ce57-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="1ce57-110">Wenn das **ulFlags-Element** des  _lpAdrParms-Parameters_ bei der Ausgabe auf DIALOG_SDI festgelegt ist, wird das Fensterhandle des Dialogfelds ohne Modus zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ce57-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="1ce57-111">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="1ce57-111">See Remarks.</span></span> 
    
 <span data-ttu-id="1ce57-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="1ce57-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="1ce57-113">[in, out] Ein Zeiger auf eine [ADRPARM-Struktur,](adrparm.md) die die Präsentation und das Verhalten des Adressdialogfelds steuert.</span><span class="sxs-lookup"><span data-stu-id="1ce57-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="1ce57-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="1ce57-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="1ce57-115">[in, out] Ein Zeiger auf einen Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die Empfängerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="1ce57-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="1ce57-116">Bei der Eingabe kann dieser Parameter NULL sein oder auf einen gültigen Zeiger zeigen.</span><span class="sxs-lookup"><span data-stu-id="1ce57-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="1ce57-117">Bei der Ausgabe zeigt dieser Parameter auf einen Zeiger auf gültige Empfängerinformationen.</span><span class="sxs-lookup"><span data-stu-id="1ce57-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ce57-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ce57-118">Return value</span></span>

<span data-ttu-id="1ce57-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ce57-119">S_OK</span></span> 
  
> <span data-ttu-id="1ce57-120">Das Dialogfeld allgemeine Adresse wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1ce57-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ce57-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ce57-121">Remarks</span></span>

<span data-ttu-id="1ce57-122">Wenn **das ulFlags-Element** des  _lpAdrParms-Parameters_ auf DIALOG_SDI vor der Rückgabe des Fensterhandle des moduslosen Dialogfelds für die Ausgabe festgelegt ist, wird es in Outlook ignoriert. Die modale Version des Dialogfelds wird immer in Nicht-Outlook-Clients angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1ce57-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="1ce57-123">Die von MAPI an den Aufrufer über den _lppAdrList-Parameter_ übergebene **ADRLIST-Struktur** enthält ein Array von [ADRENTRY-Strukturen,](adrentry.md) eine Struktur für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="1ce57-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="1ce57-124">Wenn sie an die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) einer ausgehenden Nachricht im  _lpMods-Parameter_ übergeben wird, kann die **ADRLIST-Struktur** verwendet werden, um die Empfängerliste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1ce57-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="1ce57-125">Jede **ADRENTRY-Struktur** in der **ADRLIST-Struktur** enthält null oder mehr [SPropValue-Strukturen,](spropvalue.md) eine Struktur für jede Eigenschaft, die für den Empfänger festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1ce57-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="1ce57-126">**SPropValue-Strukturen** können null sein, wenn das von der **Address-Methode** angezeigte Dialogfeld zum Entfernen eines Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ce57-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="1ce57-127">Wenn eine oder mehrere **SPropValue-Strukturen** verfügbar sind, wird die entsprechende **ADRENTRY-Struktur** zum Hinzufügen oder Aktualisieren eines Empfängers verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ce57-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="1ce57-128">Der Empfänger kann aufgelöst werden, was angibt, dass eine der **SPropValue-Strukturen** die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft des Empfängers beschreibt, oder nicht aufgelöst, was angibt, dass die **PR_ENTRYID-Eigenschaft** fehlt.</span><span class="sxs-lookup"><span data-stu-id="1ce57-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="1ce57-129">Zusätzlich zu **PR_ENTRYID** enthalten aufgelöste Empfänger die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1ce57-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="1ce57-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ce57-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1ce57-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ce57-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="1ce57-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ce57-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1ce57-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ce57-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="1ce57-134">Die **ADRLIST-Struktur,** die der Aufrufer übergibt, kann eine andere Größe als die von MAPI zurückgegebene Struktur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1ce57-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="1ce57-135">Wenn MAPI eine größere **ADRLIST-Struktur** zurückgeben muss, wird die ursprüngliche Struktur frei und eine neue zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1ce57-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="1ce57-136">Wenn Sie speicher für die **ADRLIST-Struktur zuweisen,** weisen Sie den Arbeitsspeicher für jede **SPropValue-Struktur** separat zu.</span><span class="sxs-lookup"><span data-stu-id="1ce57-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="1ce57-137">Weitere Informationen zum Zuordnen und Freispeichern von **ADRLIST-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="1ce57-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="1ce57-138">**Address** gibt sofort zurück, wenn das DIALOG_SDI im **ulFlags-Element** der **ADRPARM-Struktur** im  _lpAdrParms-Parameter festgelegt_ ist.</span><span class="sxs-lookup"><span data-stu-id="1ce57-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="1ce57-139">Das DIALOG_SDI wird für Nicht-Outlook-Clients ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1ce57-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="1ce57-140">Wenn DIALOG_SDI ignoriert wird, wird die modale Version des Dialogfelds angezeigt, und ein Zeiger auf ein Handle sollte in _lpulUIParam nicht erwartet werden._</span><span class="sxs-lookup"><span data-stu-id="1ce57-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="1ce57-141">**Address** unterstützt Unicode-Zeichenzeichenfolgen in der **ADRPARM-Struktur,** wenn AB_UNICODEUI im **ulFlags-Element** von **ADRPARM** im _lpAdrParms-Parameter_ angegeben wurde, und es werden Unicode-Zeichenzeichenfolgen in **ADRLIST unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="1ce57-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="1ce57-142">Die Unicode-Zeichenfolgen werden in das MbCS-Format (Multibyte Character String) konvertiert, bevor sie im Dialogfeld Outlook-Adressbuch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce57-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ce57-143">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1ce57-143">MFCMAPI reference</span></span>

<span data-ttu-id="1ce57-144">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1ce57-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ce57-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1ce57-145">**File**</span></span>|<span data-ttu-id="1ce57-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1ce57-146">**Function**</span></span>|<span data-ttu-id="1ce57-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1ce57-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ce57-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1ce57-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1ce57-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="1ce57-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="1ce57-150">MFCMAPI verwendet die **Address-Methode,** damit der Benutzer auswählen kann, welches Postfach geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ce57-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ce57-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ce57-151">See also</span></span>



[<span data-ttu-id="1ce57-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="1ce57-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="1ce57-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="1ce57-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="1ce57-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="1ce57-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="1ce57-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="1ce57-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="1ce57-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="1ce57-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="1ce57-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1ce57-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1ce57-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="1ce57-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="1ce57-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1ce57-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1ce57-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1ce57-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="1ce57-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1ce57-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1ce57-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1ce57-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1ce57-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1ce57-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1ce57-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1ce57-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="1ce57-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1ce57-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1ce57-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1ce57-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

