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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3edcef69880dbc2a566a44582113c43802a47324
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792518"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="41ae2-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="41ae2-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="41ae2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41ae2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41ae2-105">Hinzugefügt, gelöscht oder Empfänger der Nachricht �ndert.</span><span class="sxs-lookup"><span data-stu-id="41ae2-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="41ae2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41ae2-106">Parameters</span></span>

 <span data-ttu-id="41ae2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41ae2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="41ae2-108">[in] Bitmaske aus Flags, die die Empfänger Änderungen steuert.</span><span class="sxs-lookup"><span data-stu-id="41ae2-108">[in] Bitmask of flags that controls the recipient changes.</span></span> <span data-ttu-id="41ae2-109">Wenn 0 (null) für den _UlFlags_ -Parameter übergeben wird, alle vorhandenen Empfänger von **ModifyRecipients** durch die Empfängerliste auf das durch den Parameter _LpMods_ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="41ae2-109">If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter.</span></span> <span data-ttu-id="41ae2-110">Die folgenden Kennzeichen können für _UlFlags_festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="41ae2-110">The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="41ae2-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="41ae2-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="41ae2-112">Die Empfänger auf die durch den Parameter  _lpMods_ sollte die Empfängerliste hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="41ae2-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="41ae2-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="41ae2-p102">Die Empfänger auf die durch den Parameter  _lpMods_ sollten bereits vorhandene Empfänger ersetzen. Alle vorhandenen Eigenschaften werden durch die in der entsprechenden [ADRENTRY](adrentry.md) Struktur ersetzt.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p102">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients. All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="41ae2-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="41ae2-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="41ae2-117">Aus der Empfängerliste mithilfe als Index der **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))-Eigenschaft, die im Array Eigenschaft Wert für jeden Empfänger Eintrag in der _LpMods_ -Parameter enthalten sollte bereits vorhandene Empfänger entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="41ae2-118">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="41ae2-118">_lpMods_</span></span>
  
> <span data-ttu-id="41ae2-119">[in] Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die eine Liste der Empfänger hinzugefügt, gelöscht oder geändert werden, in der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="41ae2-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41ae2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41ae2-120">Return value</span></span>

<span data-ttu-id="41ae2-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="41ae2-121">S_OK</span></span> 
  
> <span data-ttu-id="41ae2-122">Die Empfängerliste wurde erfolgreich geändert.</span><span class="sxs-lookup"><span data-stu-id="41ae2-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41ae2-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41ae2-123">Remarks</span></span>

<span data-ttu-id="41ae2-p103">Die **IMessage::ModifyRecipients** -Methode �ndert die Nachricht Empfängerliste. Es ist in dieser Liste gehalten in eine [ADRLIST](adrlist.md) -Struktur, dass die Empfänger Tabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p103">The **IMessage::ModifyRecipients** method changes the message's recipient list. It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="41ae2-126">Die **ADRLIST** -Datenstruktur enthält eine [ADRENTRY](adrentry.md) -Struktur für jeden Empfänger und jede **ADRENTRY** -Datenstruktur enthält ein Array der Eigenschaftswerte, die die Empfängereigenschaften beschreibt.</span><span class="sxs-lookup"><span data-stu-id="41ae2-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="41ae2-127">Empfänger in der Struktur **ADRLIST** können gelöst oder nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="41ae2-128">Der Unterschied liegt in der Anzahl und Typ der Eigenschaften, die eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="41ae2-129">Ein nicht aufgelöster Empfänger enthält nur die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) Eigenschaften während ein aufgelöster Empfänger, die zwei Eigenschaften sowie **PR_ADDRTYPE enthält **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) und **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41ae2-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="41ae2-130">Wenn **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) zur Verfügung steht, können sie auch berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="41ae2-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="41ae2-p105">Durch die Zeit, die eine Nachricht gesendet wird, muss nur aufgelösten Empfänger in der Empfängerliste enthalten. Nicht aufgelösten Empfänger verursachen Unzustellbarkeitsberichten erstellt und an den ursprünglichen Absender der Nachricht gesendet werden. Weitere Informationen zu den Vorgang der Namensaufl�sung aus Sicht des Clients finden Sie unter [Aufl�sen von Namen](resolving-a-recipient-name.md). Weitere Informationen aus der Perspektive der Adressbuchanbieter finden Sie unter [Implementieren der Namensaufl�sung](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="41ae2-p105">By the time a message is submitted, it must include only resolved recipients in its recipient list. Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message. For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md). For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="41ae2-p106">Nicht aufgelöst und nicht aufgelösten Empfänger kann ein Empfänger NULL sein. Das **cValues** Mitglied der **ADRENTRY** -Struktur für den Empfänger auf 0 (null) festgelegt ist und der **rgPropVals** Member wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p106">In addition to resolved and unresolved recipients, a recipient can be NULL. The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="41ae2-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="41ae2-137">Notes to callers</span></span>

<span data-ttu-id="41ae2-p107">Sie können eine Empfängerliste durch Aufrufen von [IAddrBook::Address](imapisupport-address.md) zum Anzeigen des Standarddialogfelds und der Benutzer aufgefordert, wählen Sie Einträge erstellen. Die Adressliste auf die durch den Parameter  _lppAdrList_ auf **Address** kann an **ModifyRecipients** als  _lpMods_ -Parameter Übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p107">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries. The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="41ae2-p108">Wenn Sie Eigenschaften für einen Empfänger in der Struktur [ADRLIST](adrlist.md) angeben, schließen Sie alle Eigenschaften des Empfängers, nicht nur diejenigen neuen oder geänderten. Wenn Sie ein Empfänger geändert wird, werden alle Eigenschaften, die nicht in der Struktur **ADRLIST** enthalten gelöscht. Zum Abrufen der aktuellen Gruppe von Eigenschaften für alle Empfänger einer Nachricht [GetRecipientTable](imessage-getrecipienttable.md) aufrufen und Abrufen von allen Zeilen. Da ein **SRowSet** dieselbe Struktur wie eine **ADRLIST**ist, können Sie diese austauschbar verwenden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p108">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones. When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted. To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows. Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="41ae2-144">**ModifyRecipients** ersetzt alle Einträge in der aktuellen Empfängerliste mit den Informationen, die auf den  _lpMods_, wenn keines der Flags im  _ulFlags_ -Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="41ae2-145">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="41ae2-145">Notes to callers</span></span>

<span data-ttu-id="41ae2-p109">Wenn Sie das MODRECIP_MODIFY-Flag festlegen, ersetzt **ModifyRecipients** jedes Empfängers gesamte Zeile mit der zugeordneten Zeile in der [ADRLIST](adrlist.md) -Struktur in  _lpMods_Übergeben. Achten Sie darauf, dass alle Eigenschaften angeben, die ein Empfänger haben sollen, ungefähre davon, ob sie geändert haben, um zu verhindern, dass Sie versehentlich gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p109">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_. Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="41ae2-148">Es folgen einige Regeln zum Festlegen der Eigenschaften der Empfänger in der Struktur **ADRLIST**:</span><span class="sxs-lookup"><span data-stu-id="41ae2-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="41ae2-p110">Verwenden Sie PT_NULL nicht als einen Eigenschaftentyp aus. **ModifyRecipients** gibt einen Fehler zurück, wenn dieser Wert auftreten.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p110">Do not use PT_NULL as a property type. **ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="41ae2-p111">Verwenden Sie PT_ERROR nicht als einen Eigenschaftentyp aus. **ModifyRecipients** wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p111">Do not use PT_ERROR as a property type. **ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="41ae2-153">Fügen Sie die **PR_ROWID** -Eigenschaft für alle Empfänger in _UlFlags_legen Sie die MODRECIP_REMOVE oder MODRECIP_MODIFY-Flag.</span><span class="sxs-lookup"><span data-stu-id="41ae2-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="41ae2-154">Schlie�en Sie die **PR_ROWID** -Eigenschaft nicht für alle Empfänger beim Festlegen der MODRECIP_ADD-Flag in  _ulFlags_ oder wenn Sie NULL in  _ulFlags_Übergeben.</span><span class="sxs-lookup"><span data-stu-id="41ae2-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="41ae2-p112">Wenn Sie die **PR_ADDRTYPE** -Eigenschaft oder die **PR_EMAIL_ADDRESS** -Eigenschaft für einen Empfänger und eine oder beide Eigenschaften sind inkonsistent mit den Adresstyp und die Adresse des Empfängers durch **PR_ENTRYID**bezeichnet, sind die Ergebnisse nicht definiert. D. h., gibt es drei Möglichkeiten, je nach Dienstanbieter:</span><span class="sxs-lookup"><span data-stu-id="41ae2-p112">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined. That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="41ae2-157">Die Nachricht wird an die Adresse, die von den Eigenschaften **PR_ADDRTYPE** und **PR_EMAIL_ADDRESS** beschriebenen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="41ae2-158">Die Nachricht wird an den Empfänger durch **PR_ENTRYID**identifizierten übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="41ae2-159">Die Nachricht wird aufgrund der Mehrdeutigkeit der Adressinformationen unzustellbar deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="41ae2-p113">Verwenden Sie die Regeln für die Zuweisung in [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md) beschriebenen Speicherzuordnung für die Empfängerliste. **ModifyRecipients** Freigabe nicht die Struktur **ADRLIST** noch keines der Unterstrukturen frei. Die Struktur **ADRLIST** und jede [SPropValue](spropvalue.md) Struktur müssen separat mithilfe der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) so, dass jeweils einzeln freigegeben werden zugeordnet werden. Wenn die Methode zusätzlichen Speicherplatz für alle **SPropValue** Struktur erfordert, kann es die **SPropValue** -Struktur mit einer neuen ersetzen, die später mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden können. **SPropValue** Originalstruktur sollten auch mithilfe der **MAPIFreeBuffer**freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41ae2-p113">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list. **ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures. The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually. If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md). The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41ae2-165">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="41ae2-165">MFCMAPI reference</span></span>

<span data-ttu-id="41ae2-166">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="41ae2-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41ae2-167">**Datei**</span><span class="sxs-lookup"><span data-stu-id="41ae2-167">**File**</span></span>|<span data-ttu-id="41ae2-168">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="41ae2-168">**Function**</span></span>|<span data-ttu-id="41ae2-169">**Comment**</span><span class="sxs-lookup"><span data-stu-id="41ae2-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41ae2-170">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="41ae2-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="41ae2-171">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="41ae2-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="41ae2-172">MFCMAPI (engl.) verwendet die **IMessage::ModifyRecipients** -Methode, um einen neuen Empfänger einer Nachricht hinzuf�gen.</span><span class="sxs-lookup"><span data-stu-id="41ae2-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41ae2-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41ae2-173">See also</span></span>



[<span data-ttu-id="41ae2-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="41ae2-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="41ae2-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="41ae2-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="41ae2-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="41ae2-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="41ae2-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="41ae2-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="41ae2-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="41ae2-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="41ae2-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="41ae2-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="41ae2-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="41ae2-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="41ae2-181">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="41ae2-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="41ae2-182">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="41ae2-182">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

