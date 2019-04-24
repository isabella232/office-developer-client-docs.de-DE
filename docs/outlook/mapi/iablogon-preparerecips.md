---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348944"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="6881a-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="6881a-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="6881a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6881a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6881a-105">Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.</span><span class="sxs-lookup"><span data-stu-id="6881a-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="6881a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6881a-106">Parameters</span></span>

<span data-ttu-id="6881a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6881a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6881a-108">in Eine Bitmaske von Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="6881a-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="6881a-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6881a-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="6881a-110">MAPI_CACHE_ONLY: Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="6881a-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="6881a-111">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6881a-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="6881a-112">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6881a-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6881a-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="6881a-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="6881a-114">in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften anzeigen, die eine Aktualisierung erfordern, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6881a-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="6881a-115">Der _lpPropTagArray_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6881a-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="6881a-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="6881a-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="6881a-117">in Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Empfängerliste enthält.</span><span class="sxs-lookup"><span data-stu-id="6881a-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6881a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6881a-118">Return value</span></span>

<span data-ttu-id="6881a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6881a-119">S_OK</span></span> 
  
> <span data-ttu-id="6881a-120">Die Empfängerliste wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="6881a-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="6881a-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6881a-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6881a-122">Mindestens einer der Empfänger im _lpRecipList_ -Parameter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6881a-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6881a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6881a-123">Return value</span></span>

<span data-ttu-id="6881a-124">Ein Client ruft die MAPI- [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) -Methode auf, um eine Gruppe von Eigenschaften für einen oder mehrere Empfänger zu ändern oder neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6881a-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="6881a-125">Die Empfänger sind möglicherweise Teil der Empfängerliste einer ausgehenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6881a-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="6881a-126">MAPI übergibt diesen Aufruf an die **IABLogon::P reparerecips** -Methode eines Adressbuch Anbieters.</span><span class="sxs-lookup"><span data-stu-id="6881a-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="6881a-127">**IABLogon::P reparerecips** führt vier Hauptaufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="6881a-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="6881a-128">Stellt sicher, dass alle Empfänger in der Adressliste, auf die durch den _lpRecipList_ -Parameter verwiesen wird, einen langfristigen Eintragsbezeichner aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6881a-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="6881a-129">Stellt sicher, dass alle Empfänger über die Eigenschaften verfügen, die im Eigenschafts Wertarray angegeben sind, auf das durch den _lpPropTagArray_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6881a-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="6881a-130">Stellt sicher, dass die Eigenschaften aus dem Eigenschafts Wertarray vor allen anderen Eigenschaften angezeigt werden, die vor dem Aufruf vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="6881a-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="6881a-131">Stellt sicher, dass die Reihenfolge der Eigenschaften in der [](adrentry.md) **ADRLIST** -Struktur der einzelnen Empfänger mit dem Wert des Eigenschaftswerts übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6881a-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="6881a-132">Die \*\*\*\* _lpRecipList_ -Parameter enthält eine **Miet** Struktur für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="6881a-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="6881a-133">Jede **Miet** Struktur enthält ein Array von [SPropValue](spropvalue.md) -Strukturen, um die Eigenschaften des Empfängers zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6881a-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="6881a-134">Wenn **IABLogon::P reparerecips** zurückgibt, enthält das **SPropValue** -Strukturarray für jeden Empfänger die Eigenschaften aus dem _lpPropTagArray_ , gefolgt von den anderen Eigenschaften für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="6881a-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6881a-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="6881a-135">Notes to implementers</span></span>

<span data-ttu-id="6881a-136">Die Implementierung von **IABLogon::P reparerecips** umfasst das Platzieren von Eigenschaften in einer bestimmten Reihenfolge, das Abrufen von Eigenschaftswerten und das Konvertieren von kurzfristigen Eintrags Bezeichnern in langfristige Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6881a-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="6881a-137">Die Eigenschaften, die im _lpPropTagArray_ -Parameter angefordert werden, müssen sich am Anfang des Eigenschafts Wertarrays befinden, das der **Miet** Struktur jedes Empfängers im _lpRecipList_ -Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6881a-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="6881a-138">Wenn keine Werte für diese Eigenschaften vorhanden sind, öffnen Sie den zugeordneten Messagingbenutzer oder die zugehörige Verteilerliste unter Verwendung der Eintrags-ID, und rufen Sie die fehlenden Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="6881a-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="6881a-139">Ordnen Sie jede **SPropValue** -Struktur, die in _lpRecipList_ übergeben wird, separat zu, damit die Strukturen einzeln freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="6881a-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="6881a-140">Wenn Sie einen zusätzlichen Speicherplatz für eine **SPropValue** -Struktur zuweisen müssen, beispielsweise zum Speichern der Daten für eine String-Eigenschaft, verwenden Sie die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, um zusätzlichen Speicherplatz für das Array der vollständigen Eigenschaftswerte zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="6881a-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="6881a-141">Verwenden Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, um das ursprüngliche Eigenschaftswert Array freizugeben, und verwenden Sie dann die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, um zusätzlichen erforderlichen Arbeitsspeicher zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="6881a-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="6881a-142">Gehen Sie folgendermaßen vor, um **IABLogon::P Reparerecips**zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="6881a-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="6881a-143">Suchen Sie nach Einträgen im _lpPropTagArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6881a-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="6881a-144">Wenn das Eigenschaftswert Array leer ist, gibt es keine Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="6881a-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="6881a-145">Zurückgeben eines Erfolgs Werts.</span><span class="sxs-lookup"><span data-stu-id="6881a-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="6881a-146">Verarbeiten Sie jeden Empfänger im _lpRecipList_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6881a-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="6881a-147">Für jeden Empfänger in der Liste gibt es ein Mitglied der **Miet** Struktur.</span><span class="sxs-lookup"><span data-stu-id="6881a-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="6881a-148">Die folgenden Empfängertypen werden ignoriert:</span><span class="sxs-lookup"><span data-stu-id="6881a-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="6881a-149">Empfänger ohne Eintragsbezeichner im **rgPropVals** -Element ihrer **Miet** Struktur (also nicht aufgelöste Empfänger).</span><span class="sxs-lookup"><span data-stu-id="6881a-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="6881a-150">Empfänger mit einer Eintrags-ID, die nicht zu Ihrem Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="6881a-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="6881a-151">Diese Empfänger werden an einen anderen Adressbuchanbieter weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6881a-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="6881a-152">Öffnen Sie den Empfänger, und rufen Sie die Eigenschaften ab, die bereits für den Empfänger festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="6881a-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="6881a-153">Zusammenführen des in der _lpRecipList_ angegebenen Eigenschafts Wertarrays mit dem Array von Eigenschaften, die von GetProps zurückgegeben werden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6881a-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="6881a-154">Wenn die gleiche Eigenschaft in beiden Eigenschaften Arrays auftritt, verwenden Sie den Wert aus _lpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="6881a-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="6881a-155">Wenn das _lpRecipList_ -Eigenschaftenwert Array groß genug ist, um alle erforderlichen Eigenschaften zu speichern, ersetzen Sie es durch das zusammengeführte Array.</span><span class="sxs-lookup"><span data-stu-id="6881a-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="6881a-156">Wenn das _lpRecipList_ -Eigenschaftswert-Array nicht groß genug ist, ersetzen Sie es durch ein neu zugeordnetes Array.</span><span class="sxs-lookup"><span data-stu-id="6881a-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="6881a-157">Stellen Sie sicher, dass das neue Array in jedem seiner **cValues** -Mitglieder über einen aktualisierten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="6881a-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="6881a-158">Wenn Sie eine oder mehrere der Eigenschaften im _lpPropTagArray_ -Parameter nicht erkennen, legen Sie den Eigenschaftentyp in der **Miet** Struktur des Empfängers auf PT_ERROR und den Eigenschaftswert entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert fest, der mehr ein bestimmter Grund für die Nichtverfügbarkeit der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6881a-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="6881a-159">Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="6881a-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="6881a-160">Ordnen Sie die **ADRLIST** -Struktur, die an IABLogon übergeben wird, nie neu zu **::P reparerecips** , oder ändern Sie die Anzahl der Einträge.</span><span class="sxs-lookup"><span data-stu-id="6881a-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6881a-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6881a-161">See also</span></span>

- [<span data-ttu-id="6881a-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="6881a-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="6881a-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6881a-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="6881a-164">Kanonische PidTagEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6881a-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="6881a-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6881a-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="6881a-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6881a-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

