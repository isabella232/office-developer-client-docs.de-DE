---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415271"
---
# <a name="entryid"></a><span data-ttu-id="97af8-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="97af8-103">ENTRYID</span></span>

  
  
<span data-ttu-id="97af8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97af8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97af8-105">Enthält einen Eintragsbezeichner für ein MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="97af8-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97af8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="97af8-106">Header file:</span></span>  <br/> |<span data-ttu-id="97af8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97af8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="97af8-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="97af8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="97af8-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="97af8-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="97af8-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="97af8-110">Members</span></span>

 <span data-ttu-id="97af8-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="97af8-111">**abFlags**</span></span>
  
> <span data-ttu-id="97af8-112">Bitmaske von Flags, die Informationen bereitstellen, die das Objekt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="97af8-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="97af8-113">Nur das erste Byte der Flags, **abFlags[0]**, kann vom Anbieter festgelegt werden. die anderen drei sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="97af8-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="97af8-114">Diese Kennzeichen dürfen nicht für permanente Eintragsbezeichner festgelegt werden. sie werden nur für kurzfristige Eintragsbezeichner festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97af8-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="97af8-115">Für Clients ist diese Struktur schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="97af8-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="97af8-116">Die folgenden Flags können in **abFlags[0]** festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="97af8-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="97af8-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="97af8-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="97af8-118">Der Eintragsbezeichner kann nicht als Empfänger für eine Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97af8-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="97af8-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="97af8-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="97af8-120">Andere Benutzer können nicht auf die Eintrags-ID zugreifen.</span><span class="sxs-lookup"><span data-stu-id="97af8-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="97af8-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="97af8-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="97af8-122">Der Eintragsbezeichner kann zu anderen Zeiten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97af8-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="97af8-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="97af8-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="97af8-124">Der Eintragsbezeichner ist kurzfristig.</span><span class="sxs-lookup"><span data-stu-id="97af8-124">The entry identifier is short-term.</span></span> <span data-ttu-id="97af8-125">Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="97af8-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="97af8-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="97af8-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="97af8-127">Der Eintragsbezeichner kann nicht für andere Sitzungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97af8-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="97af8-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="97af8-128">**ab**</span></span>
  
> <span data-ttu-id="97af8-129">Gibt ein Array von Binärdaten an, das von Dienstanbietern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97af8-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="97af8-130">Die Clientanwendung kann dieses Array nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="97af8-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97af8-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97af8-131">Remarks</span></span>

<span data-ttu-id="97af8-132">Die **ENTRYID-Struktur** wird von Nachrichtenspeicher- und Adressbuchanbietern verwendet, um eindeutige Bezeichner für ihre Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="97af8-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="97af8-133">Eingabebezeichner werden verwendet, um die folgenden Objekttypen zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="97af8-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="97af8-134">Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="97af8-134">Message stores</span></span>
    
- <span data-ttu-id="97af8-135">Ordner</span><span class="sxs-lookup"><span data-stu-id="97af8-135">Folders</span></span>
    
- <span data-ttu-id="97af8-136">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="97af8-136">Messages</span></span>
    
- <span data-ttu-id="97af8-137">Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="97af8-137">Address book containers</span></span>
    
- <span data-ttu-id="97af8-138">Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="97af8-138">Distribution lists</span></span>
    
- <span data-ttu-id="97af8-139">Messagingbenutzer</span><span class="sxs-lookup"><span data-stu-id="97af8-139">Messaging users</span></span>
    
- <span data-ttu-id="97af8-140">Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="97af8-140">Status objects</span></span>
    
- <span data-ttu-id="97af8-141">Profilabschnitte</span><span class="sxs-lookup"><span data-stu-id="97af8-141">Profile sections</span></span>
    
<span data-ttu-id="97af8-142">Jeder Anbieter verwendet ein Format für die **ENTRYID-Struktur,** das für diesen Anbieter sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="97af8-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="97af8-143">Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="97af8-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="97af8-144">Um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen, rufen Sie die [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) auf.</span><span class="sxs-lookup"><span data-stu-id="97af8-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="97af8-145">Wenn ein Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts aufruft, um den Eintragsbezeichner abzurufen, gibt das Objekt die dauerhafteste Form der Eintrags-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="97af8-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="97af8-146">Ein Client kann überprüfen, ob ein Eintragsbezeichner langfristig ist, indem er überprüft, ob keines der Kennzeichen im ersten Byte des **abFlags-Mitglieds festgelegt** ist.</span><span class="sxs-lookup"><span data-stu-id="97af8-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="97af8-147">Wenn ein Client über eine Spalte in einer Tabelle auf einen Eintragsbezeichner zutritt, ist dieser Eintragsbezeichner höchstwahrscheinlich kurz- statt langfristig.</span><span class="sxs-lookup"><span data-stu-id="97af8-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="97af8-148">Kurzfristige Eintragsbezeichner können nur in der aktuellen MAPI-Sitzung verwendet werden, um die entsprechenden Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97af8-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="97af8-149">Ein Client kann überprüfen, ob ein Eintragsbezeichner kurzfristig ist, indem er überprüft, ob alle Kennzeichen im ersten Byte des **abFlags-Mitglieds festgelegt** sind.</span><span class="sxs-lookup"><span data-stu-id="97af8-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="97af8-150">Einige Eintragsbezeichner sind kurzfristig, haben aber eine langfristige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="97af8-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="97af8-151">Für einen solchen Eintragsbezeichner wird mindestens eines der entsprechenden Flags im ersten Byte des **abFlags-Mitglieds festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="97af8-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="97af8-152">Eine **ENTRYID-Struktur** ähnelt einer [FLATENTRY-Struktur.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="97af8-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="97af8-153">Es gibt jedoch einige Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="97af8-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="97af8-154">In **einer ENTRYID-Struktur** wird die Größe der Eintrags-ID nicht gespeichert. eine **FLATENTRY-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="97af8-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="97af8-155">Eine **ENTRYID-Struktur** speichert die Kennzeichendaten und den Rest der Eintrags-ID separat. Eine **FLATENTRY-Struktur** speichert die Kennzeichendaten mit dem Rest der Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="97af8-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="97af8-156">Eine **ENTRYID-Struktur** wird als Parameter an die Methoden der [IMAPIProp-Schnittstelle](imapipropiunknown.md) und an die folgenden **OpenEntry-Methoden** übergeben: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="97af8-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="97af8-157">Eine **ENTRYID-Struktur** wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="97af8-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="97af8-158">Eine **FLATENTRY-Struktur** wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder sie in einem Bytestrom zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="97af8-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="97af8-159">Clients sollten immer natürlich ausgerichtete Eintragsbezeichner übergeben.</span><span class="sxs-lookup"><span data-stu-id="97af8-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="97af8-160">Obwohl Anbieter willkürlich ausgerichtete Eintragsbezeichner behandeln sollten, sollten Clients dieses Verhalten nicht erwarten.</span><span class="sxs-lookup"><span data-stu-id="97af8-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="97af8-161">Wenn eine gute ausgerichtete Eintrags-ID nicht an eine Methode übergeben wird, kann dies zu einem Ausrichtungsfehler bei RISC-Prozessoren führen.</span><span class="sxs-lookup"><span data-stu-id="97af8-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="97af8-162">Der natürliche Ausrichtungsfaktor (in der Regel 8 Byte) ist der größte datentyp, der von der CPU unterstützt wird, und in der Regel der gleiche Ausrichtungsfaktor, der von der Systemspeicherzuweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97af8-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="97af8-163">Eine natürlich ausgerichtete Speicheradresse ermöglicht der CPU den Zugriff auf jeden datentyp, den sie an dieser Adresse unterstützt, ohne einen Ausrichtungsfehler zu generieren.</span><span class="sxs-lookup"><span data-stu-id="97af8-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="97af8-164">Für RISC-CPUs muss ein Datentyp der Größe N Bytes in der Regel an einem geraden Vielfachen von N Bytes ausgerichtet werden, bei der Adresse ist ein gerades Vielfaches von N.</span><span class="sxs-lookup"><span data-stu-id="97af8-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="97af8-165">Weitere Informationen finden Sie unter [Entry Identifiers](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="97af8-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97af8-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97af8-166">See also</span></span>



[<span data-ttu-id="97af8-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="97af8-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="97af8-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="97af8-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="97af8-169">PidTagRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="97af8-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="97af8-170">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="97af8-170">MAPI Structures</span></span>](mapi-structures.md)

