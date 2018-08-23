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
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589742"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="efdf5-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="efdf5-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="efdf5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efdf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efdf5-105">Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.</span><span class="sxs-lookup"><span data-stu-id="efdf5-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="efdf5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="efdf5-106">Parameters</span></span>

<span data-ttu-id="efdf5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efdf5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="efdf5-108">[in] Eine Bitmaske aus Flags, die den Typ des Texts in der zurückgegebenen Zeichenfolge steuert.</span><span class="sxs-lookup"><span data-stu-id="efdf5-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="efdf5-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="efdf5-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="efdf5-110">MAPI_CACHE_ONLY: Verwenden Sie nur das Offlineadressbuch namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="efdf5-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="efdf5-111">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="efdf5-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="efdf5-112">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="efdf5-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="efdf5-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="efdf5-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="efdf5-114">[in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags, die die Eigenschaften, die aktualisieren enthält angeben, wenn erfordern.</span><span class="sxs-lookup"><span data-stu-id="efdf5-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="efdf5-115">Der Parameter _LpPropTagArray_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="efdf5-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="efdf5-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="efdf5-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="efdf5-117">[in] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Empfängerliste enthält.</span><span class="sxs-lookup"><span data-stu-id="efdf5-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="efdf5-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="efdf5-118">Return value</span></span>

<span data-ttu-id="efdf5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="efdf5-119">S_OK</span></span> 
  
> <span data-ttu-id="efdf5-120">Die Empfängerliste wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="efdf5-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="efdf5-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="efdf5-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="efdf5-122">Eine oder mehrere Empfänger in der _LpRecipList_ -Parameter sind nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="efdf5-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="efdf5-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="efdf5-123">Return value</span></span>

<span data-ttu-id="efdf5-124">Ein Client Ruft die MAPI- [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) -Methode zum Ändern oder neu anordnen eine Reihe von Eigenschaften für einen oder mehrere Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="efdf5-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="efdf5-125">Der Empfänger können oder möglicherweise nicht Teil der Liste der Empfänger von ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="efdf5-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="efdf5-126">MAPI überträgt dieses Anrufs an eine Adressbuchanbieter **IABLogon::PrepareRecips** -Methode.</span><span class="sxs-lookup"><span data-stu-id="efdf5-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="efdf5-127">**IABLogon::PrepareRecips** werden die vier Wichtigste Aufgaben ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="efdf5-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="efdf5-128">Stellt sicher, dass alle Empfänger in der Adressliste verwiesen durch den Parameter _LpRecipList_ langfristige Eintrags-ID verfügen.</span><span class="sxs-lookup"><span data-stu-id="efdf5-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="efdf5-129">Stellt sicher, dass alle Empfänger die Eigenschaften den Wert Array-Eigenschaft auf das durch den Parameter _LpPropTagArray_ angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="efdf5-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="efdf5-130">Stellt sicher, dass die Eigenschaften aus dem Array der Eigenschaft Wert vor alle anderen Eigenschaften werden angezeigt, die vor dem Aufruf vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="efdf5-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="efdf5-131">Stellt sicher, dass die Reihenfolge der Eigenschaften des Empfängers [ADRENTRY](adrentry.md) Struktur in der Struktur **ADRLIST** Array der Wert-Eigenschaft identisch ist.</span><span class="sxs-lookup"><span data-stu-id="efdf5-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="efdf5-132">Die **ADRENTRY** -Struktur in der _LpRecipList_ -Parameter enthält eine **ADRENTRY** -Struktur für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="efdf5-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="efdf5-133">Jede **ADRENTRY** -Datenstruktur enthält ein Array von [SPropValue](spropvalue.md) -Strukturen, um die Eigenschaften des Empfängers zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="efdf5-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="efdf5-134">Wenn **IABLogon::PrepareRecips** zurückgegeben wird, enthält das **SPropValue** -Struktur-Array für jeden Empfänger die Eigenschaften aus der _LpPropTagArray_ , gefolgt von den anderen Eigenschaften für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="efdf5-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="efdf5-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="efdf5-135">Notes to implementers</span></span>

<span data-ttu-id="efdf5-136">Implementieren von **IABLogon::PrepareRecips** umfasst Eigenschaften in einer bestimmten Reihenfolge einfügen, Abrufen von Eigenschaftswerten und kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner konvertieren.</span><span class="sxs-lookup"><span data-stu-id="efdf5-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="efdf5-137">Die Eigenschaften, die im Parameter _LpPropTagArray_ angefordert werden, müssen am Anfang des Arrays der Eigenschaft Wert des Empfängers **ADRENTRY** Struktur im Parameter _LpRecipList_ zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="efdf5-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="efdf5-138">Wenn Werte für diese Eigenschaften nicht vorhanden sind, öffnen Sie die zugeordnete messaging Benutzer oder eine Verteilergruppe der angegebenen Liste mithilfe von dessen Eintrags-ID und abgerufen Sie fehlenden Werte.</span><span class="sxs-lookup"><span data-stu-id="efdf5-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="efdf5-139">Ordnen Sie jede **SPropValue** Struktur übergebenen _LpRecipList_ separat, damit die Strukturen einzeln freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="efdf5-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="efdf5-140">Wenn Sie zusätzlichen Speicherplatz für alle **SPropValue** -Struktur zuweisen müssen, beispielsweise zum Speichern der Daten für eine Zeichenfolgeneigenschaft verwenden Sie die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) zusätzlichen Speicherplatz für Wertearray vollständige-Eigenschaft zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="efdf5-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="efdf5-141">Verwenden Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion das ursprünglichen Eigenschaft Wertearray frei, und klicken Sie dann verwenden Sie die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, um alle zusätzlichen Speicher zuweisen, der erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="efdf5-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="efdf5-142">Um **IABLogon::PrepareRecips**implementieren möchten, verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="efdf5-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="efdf5-143">Überprüfen Sie die Einträge in der _LpPropTagArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="efdf5-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="efdf5-144">Wenn das Wertearray-Eigenschaft leer ist, ist gibt es keine Arbeit.</span><span class="sxs-lookup"><span data-stu-id="efdf5-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="efdf5-145">Einen Erfolgswert zurück.</span><span class="sxs-lookup"><span data-stu-id="efdf5-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="efdf5-146">Verarbeiten Sie jeden Empfänger in der _LpRecipList_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="efdf5-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="efdf5-147">Es ist ein Mitglied der **ADRENTRY** -Struktur für jeden Empfänger in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="efdf5-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="efdf5-148">Ignorieren Sie die folgenden Typen von Empfängern:</span><span class="sxs-lookup"><span data-stu-id="efdf5-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="efdf5-149">Empfänger ohne Bezeichner Eintrag im **RgPropVals** Mitglied ihrer **ADRENTRY** -Struktur (d. h., nicht aufgelösten Empfänger).</span><span class="sxs-lookup"><span data-stu-id="efdf5-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="efdf5-150">Empfänger mit einem Eintrag Bezeichner, der nicht zu Ihrem Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="efdf5-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="efdf5-151">Diese Empfänger werden an eine andere Adressbuchanbieter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="efdf5-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="efdf5-152">Öffnen Sie den Empfänger und Abrufen der Eigenschaften, die bereits für den Empfänger festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="efdf5-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="efdf5-153">Zusammenführen Sie angegebene, in der _LpRecipList_ mit dem Array von Eigenschaften von **GetProps**zurückgegebenen Array der Eigenschaft Wert.</span><span class="sxs-lookup"><span data-stu-id="efdf5-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="efdf5-154">Wenn die gleiche Eigenschaft in beiden Arrays Eigenschaft auftritt, verwenden Sie den Wert von _LpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="efdf5-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="efdf5-155">Wenn _LpRecipList_ -Eigenschaft Wertearray groß genug, um alle erforderlichen Eigenschaften enthalten ist, ersetzen Sie ihn nur durch das verbundene Array.</span><span class="sxs-lookup"><span data-stu-id="efdf5-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="efdf5-156">Wenn Wertearray der _LpRecipList_ -Eigenschaft nicht groß genug ist, ersetzen Sie ihn durch eine neu zugeordnete Array.</span><span class="sxs-lookup"><span data-stu-id="efdf5-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="efdf5-157">Stellen Sie sicher, dass für das neue Array einen aktualisierten Wert in den einzelnen Membern **cValues** ist.</span><span class="sxs-lookup"><span data-stu-id="efdf5-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="efdf5-158">Wenn Sie eine oder mehrere der Eigenschaften im _LpPropTagArray_ -Parameter nicht erkennen, legen Sie den Eigenschaftstyp in der Aufgabenliste des Empfängers zu PT_ERROR und den Wert der Eigenschaft um MAPI_E_NOT_FOUND oder auf einen anderen Wert, der eine einheitliche **ADRENTRY** -Struktur bestimmte Grund für den Ausfall der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="efdf5-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="efdf5-159">Informationen zu PT_ERROR finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="efdf5-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="efdf5-160">Nie Zuordnen der **ADRLIST** -Struktur, die in **IABLogon::PrepareRecips** übergeben wird, oder ändern Sie die Anzahl der Einträge.</span><span class="sxs-lookup"><span data-stu-id="efdf5-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efdf5-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efdf5-161">See also</span></span>

- [<span data-ttu-id="efdf5-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="efdf5-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="efdf5-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="efdf5-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="efdf5-164">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="efdf5-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="efdf5-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="efdf5-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="efdf5-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="efdf5-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

