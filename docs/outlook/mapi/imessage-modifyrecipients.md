---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 07e1c2104068a6eb242e8ba81f91655edaa92cd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426240"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="e8e29-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="e8e29-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="e8e29-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8e29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8e29-105">Hinzugef�gt, gel�scht oder Empf�nger der Nachricht �ndert.</span><span class="sxs-lookup"><span data-stu-id="e8e29-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="e8e29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8e29-106">Parameters</span></span>

 <span data-ttu-id="e8e29-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8e29-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e8e29-p101">[in] Bitmask of flags that controls the recipient changes. If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter. The following flags can be set for  _ulFlags_:</span><span class="sxs-lookup"><span data-stu-id="e8e29-p101">[in] Bitmask of flags that controls the recipient changes. If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter. The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="e8e29-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="e8e29-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="e8e29-112">Die Empf�nger auf die durch den Parameter  _lpMods_ sollte die Empf�ngerliste hinzugef�gt werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="e8e29-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e8e29-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="e8e29-p102">Die Empf�nger auf die durch den Parameter  _lpMods_ sollten bereits vorhandene Empf�nger ersetzen. Alle vorhandenen Eigenschaften werden durch die in der entsprechenden [ADRENTRY](adrentry.md) Struktur ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p102">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients. All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="e8e29-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="e8e29-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="e8e29-117">Vorhandene Empfänger sollten aus der Empfängerliste entfernt werden, indem die **PR_ROWID** ([pidtagrowid (](pidtagrowid-canonical-property.md))-Eigenschaft, die im Eigenschaftswert Array der einzelnen Empfänger Einträge im _lpMods_ -Parameter enthalten ist, als Index verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8e29-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="e8e29-118">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="e8e29-118">_lpMods_</span></span>
  
> <span data-ttu-id="e8e29-119">[in] Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die eine Liste der Empf�nger hinzugef�gt, gel�scht oder ge�ndert werden, in der Nachricht enth�lt.</span><span class="sxs-lookup"><span data-stu-id="e8e29-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8e29-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8e29-120">Return value</span></span>

<span data-ttu-id="e8e29-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8e29-121">S_OK</span></span> 
  
> <span data-ttu-id="e8e29-122">Die Empf�ngerliste wurde erfolgreich ge�ndert.</span><span class="sxs-lookup"><span data-stu-id="e8e29-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8e29-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8e29-123">Remarks</span></span>

<span data-ttu-id="e8e29-p103">Die **IMessage::ModifyRecipients** -Methode �ndert die Nachricht Empf�ngerliste. Es ist in dieser Liste gehalten in eine [ADRLIST](adrlist.md) -Struktur, dass die Empf�nger Tabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p103">The **IMessage::ModifyRecipients** method changes the message's recipient list. It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="e8e29-126">Die **ADRLIST** -Datenstruktur enth�lt eine [ADRENTRY](adrentry.md) -Struktur f�r jeden Empf�nger und jede **ADRENTRY** -Datenstruktur enth�lt ein Array der Eigenschaftswerte, die die Empf�ngereigenschaften beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8e29-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="e8e29-127">Empf�nger in der Struktur **ADRLIST** k�nnen gel�st oder nicht aufgel�st werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="e8e29-128">Der Unterschied liegt in der Anzahl und Typ der Eigenschaften, die eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="e8e29-129">Ein nicht aufgelöster Empfänger enthält nur die Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md)), während ein aufgelöst Empfänger diese beiden Eigenschaften Plus \*\*PR_ADDRTYPE \*\*([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) und **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8e29-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="e8e29-130">Wenn **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) verfügbar ist, kann es auch hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="e8e29-p105">Durch die Zeit, die eine Nachricht gesendet wird, muss nur aufgel�sten Empf�nger in der Empf�ngerliste enthalten. Nicht aufgel�sten Empf�nger verursachen Unzustellbarkeitsberichten erstellt und an den urspr�nglichen Absender der Nachricht gesendet werden. Weitere Informationen zu den Vorgang der Namensaufl�sung aus Sicht des Clients finden Sie unter [Aufl�sen von Namen](resolving-a-recipient-name.md). Weitere Informationen aus der Perspektive der Adressbuchanbieter finden Sie unter [Implementieren der Namensaufl�sung](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="e8e29-p105">By the time a message is submitted, it must include only resolved recipients in its recipient list. Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message. For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md). For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="e8e29-p106">Nicht aufgel�st und nicht aufgel�sten Empf�nger kann ein Empf�nger NULL sein. Das **cValues** Mitglied der **ADRENTRY** -Struktur f�r den Empf�nger auf 0 (null) festgelegt ist und der **rgPropVals** Member wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p106">In addition to resolved and unresolved recipients, a recipient can be NULL. The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8e29-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e8e29-137">Notes to callers</span></span>

<span data-ttu-id="e8e29-p107">Sie k�nnen eine Empf�ngerliste durch Aufrufen von [IAddrBook::Address](imapisupport-address.md) zum Anzeigen des Standarddialogfelds und der Benutzer aufgefordert, w�hlen Sie Eintr�ge erstellen. Die Adressliste auf die durch den Parameter  _lppAdrList_ auf **Address** kann an **ModifyRecipients** als  _lpMods_ -Parameter �bergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p107">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries. The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="e8e29-p108">Wenn Sie Eigenschaften f�r einen Empf�nger in der Struktur [ADRLIST](adrlist.md) angeben, schlie�en Sie alle Eigenschaften des Empf�ngers, nicht nur diejenigen neuen oder ge�nderten. Wenn Sie ein Empf�nger ge�ndert wird, werden alle Eigenschaften, die nicht in der Struktur **ADRLIST** enthalten gel�scht. Zum Abrufen der aktuellen Gruppe von Eigenschaften f�r alle Empf�nger einer Nachricht [GetRecipientTable](imessage-getrecipienttable.md) aufrufen und Abrufen von allen Zeilen. Da ein **SRowSet** dieselbe Struktur wie eine **ADRLIST**ist, k�nnen Sie diese austauschbar verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p108">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones. When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted. To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows. Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="e8e29-144">**ModifyRecipients** ersetzt alle Eintr�ge in der aktuellen Empf�ngerliste mit den Informationen, die auf den  _lpMods_, wenn keines der Flags im  _ulFlags_ -Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8e29-145">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e8e29-145">Notes to callers</span></span>

<span data-ttu-id="e8e29-p109">Wenn Sie das MODRECIP_MODIFY-Flag festlegen, ersetzt **ModifyRecipients** jedes Empf�ngers gesamte Zeile mit der zugeordneten Zeile in der [ADRLIST](adrlist.md) -Struktur in  _lpMods_�bergeben. Achten Sie darauf, dass alle Eigenschaften angeben, die ein Empf�nger haben sollen, unabh�ngig davon, ob sie ge�ndert haben, um zu verhindern, dass Sie versehentlich gel�scht wird.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p109">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_. Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="e8e29-148">Es folgen einige Regeln zum Festlegen der Eigenschaften der Empf�nger in der Struktur **ADRLIST**:</span><span class="sxs-lookup"><span data-stu-id="e8e29-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="e8e29-p110">Verwenden Sie PT_NULL nicht als einen Eigenschaftentyp aus. **ModifyRecipients** gibt einen Fehler zur�ck, wenn dieser Wert auftreten.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p110">Do not use PT_NULL as a property type. **ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="e8e29-p111">Verwenden Sie PT_ERROR nicht als einen Eigenschaftentyp aus. **ModifyRecipients** wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p111">Do not use PT_ERROR as a property type. **ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="e8e29-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e8e29-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="e8e29-154">Schlie�en Sie die **PR_ROWID** -Eigenschaft nicht f�r alle Empf�nger beim Festlegen der MODRECIP_ADD-Flag in  _ulFlags_ oder wenn Sie NULL in  _ulFlags_�bergeben.</span><span class="sxs-lookup"><span data-stu-id="e8e29-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="e8e29-p112">Wenn Sie die **PR_ADDRTYPE** -Eigenschaft oder die **PR_EMAIL_ADDRESS** -Eigenschaft f�r einen Empf�nger und eine oder beide Eigenschaften sind inkonsistent mit den Adresstyp und die Adresse des Empf�ngers durch **PR_ENTRYID**bezeichnet, sind die Ergebnisse nicht definiert. D. h., gibt es drei M�glichkeiten, je nach Dienstanbieter:</span><span class="sxs-lookup"><span data-stu-id="e8e29-p112">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined. That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="e8e29-157">Die Nachricht wird an die Adresse, die von den Eigenschaften **PR_ADDRTYPE** und **PR_EMAIL_ADDRESS** beschriebenen �bermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="e8e29-158">Die Nachricht wird an den Empf�nger durch **PR_ENTRYID**identifizierten �bermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="e8e29-159">Die Nachricht wird aufgrund der Mehrdeutigkeit der Adressinformationen unzustellbar deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="e8e29-p113">Verwenden Sie die Regeln f�r die Zuweisung in [Verwalten von Arbeitsspeicher f�r ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md) beschriebenen Speicherzuordnung f�r die Empf�ngerliste. **ModifyRecipients** Freigabe nicht die Struktur **ADRLIST** noch keines der Unterstrukturen frei. Die Struktur **ADRLIST** und jede [SPropValue](spropvalue.md) Struktur m�ssen separat mithilfe der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) so, dass jeweils einzeln freigegeben werden zugeordnet werden. Wenn die Methode zus�tzlichen Speicherplatz f�r alle **SPropValue** Struktur erfordert, kann es die **SPropValue** -Struktur mit einer neuen ersetzen, die sp�ter mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden k�nnen. **SPropValue** Originalstruktur sollten auch mithilfe der **MAPIFreeBuffer**freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e8e29-p113">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list. **ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures. The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually. If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md). The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8e29-165">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="e8e29-165">MFCMAPI reference</span></span>

<span data-ttu-id="e8e29-166">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e8e29-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8e29-167">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e8e29-167">**File**</span></span>|<span data-ttu-id="e8e29-168">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e8e29-168">**Function**</span></span>|<span data-ttu-id="e8e29-169">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e8e29-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8e29-170">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="e8e29-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e8e29-171">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="e8e29-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="e8e29-172">MFCMAPI (engl.) verwendet die **IMessage::ModifyRecipients** -Methode, um einen neuen Empf�nger einer Nachricht hinzuf�gen.</span><span class="sxs-lookup"><span data-stu-id="e8e29-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8e29-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8e29-173">See also</span></span>



[<span data-ttu-id="e8e29-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="e8e29-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="e8e29-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e8e29-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="e8e29-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="e8e29-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="e8e29-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="e8e29-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="e8e29-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e8e29-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e8e29-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e8e29-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e8e29-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e8e29-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e8e29-181">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e8e29-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="e8e29-182">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e8e29-182">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

