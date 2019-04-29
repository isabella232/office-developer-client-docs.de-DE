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
# <a name="entryid"></a><span data-ttu-id="1b39b-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1b39b-103">ENTRYID</span></span>

  
  
<span data-ttu-id="1b39b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b39b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b39b-105">Enthält eine Eintrags-ID für ein MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b39b-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b39b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1b39b-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b39b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1b39b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1b39b-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="1b39b-108">Related macros:</span></span>  <br/> |<span data-ttu-id="1b39b-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="1b39b-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="1b39b-110">Members</span><span class="sxs-lookup"><span data-stu-id="1b39b-110">Members</span></span>

 <span data-ttu-id="1b39b-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="1b39b-111">**abFlags**</span></span>
  
> <span data-ttu-id="1b39b-112">Bitmaske von Flags, die Informationen zur Beschreibung des Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b39b-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="1b39b-113">Nur das erste Byte der Flags, **abFlags [0]**, kann vom Anbieter festgelegt werden; die anderen drei sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="1b39b-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="1b39b-114">Diese Flags dürfen nicht für dauerhafte Eintragsbezeichner festgelegt werden; Sie werden nur für kurzfristige Eintrags-IDs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1b39b-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="1b39b-115">Für Clients ist diese Struktur schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1b39b-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="1b39b-116">Die folgenden Flags können in **abFlags [0]** festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1b39b-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="1b39b-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="1b39b-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="1b39b-118">Die Eintrags-ID kann nicht als Empfänger einer Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="1b39b-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="1b39b-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="1b39b-120">Andere Benutzer können nicht auf die Eintrags-ID zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1b39b-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="1b39b-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="1b39b-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="1b39b-122">Die Eintrags-ID kann nicht zu anderen Zeiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="1b39b-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="1b39b-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="1b39b-124">Die Eintrags-ID ist kurzfristig.</span><span class="sxs-lookup"><span data-stu-id="1b39b-124">The entry identifier is short-term.</span></span> <span data-ttu-id="1b39b-125">Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1b39b-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="1b39b-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="1b39b-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="1b39b-127">Die Eintrags-ID kann nicht in anderen Sitzungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="1b39b-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="1b39b-128">**ab**</span></span>
  
> <span data-ttu-id="1b39b-129">Gibt ein Array von Binärdaten an, die von Dienstanbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="1b39b-130">Die Clientanwendung kann dieses Array nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b39b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b39b-131">Remarks</span></span>

<span data-ttu-id="1b39b-132">Die **Eintrags** -ID-Struktur wird vom Nachrichtenspeicher und den Adressbuch Anbietern verwendet, um eindeutige Bezeichner für Ihre Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b39b-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="1b39b-133">Eintrags-IDs werden verwendet, um die folgenden Objekttypen zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="1b39b-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="1b39b-134">Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="1b39b-134">Message stores</span></span>
    
- <span data-ttu-id="1b39b-135">Ordner</span><span class="sxs-lookup"><span data-stu-id="1b39b-135">Folders</span></span>
    
- <span data-ttu-id="1b39b-136">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1b39b-136">Messages</span></span>
    
- <span data-ttu-id="1b39b-137">Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="1b39b-137">Address book containers</span></span>
    
- <span data-ttu-id="1b39b-138">Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="1b39b-138">Distribution lists</span></span>
    
- <span data-ttu-id="1b39b-139">Messaging Benutzer</span><span class="sxs-lookup"><span data-stu-id="1b39b-139">Messaging users</span></span>
    
- <span data-ttu-id="1b39b-140">Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="1b39b-140">Status objects</span></span>
    
- <span data-ttu-id="1b39b-141">Profilabschnitte</span><span class="sxs-lookup"><span data-stu-id="1b39b-141">Profile sections</span></span>
    
<span data-ttu-id="1b39b-142">Jeder Anbieter verwendet ein Format für die **Eintrags** -Struktur, die für diesen Anbieter sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="1b39b-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="1b39b-143">Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b39b-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="1b39b-144">Rufen Sie die [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) -Methode auf, um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen.</span><span class="sxs-lookup"><span data-stu-id="1b39b-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="1b39b-145">Wenn ein Client die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode eines Objekts zum Abrufen seiner Eintrags-ID aufruft, gibt das Objekt die dauerhaftste Form der Eintrags-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="1b39b-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="1b39b-146">Ein Client kann überprüfen, ob eine Eintrags-ID langfristig ist, indem er überprüft, ob keines der Flags im ersten Byte des **abFlags** -Members festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1b39b-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="1b39b-147">Wenn ein Client über eine Spalte in einer Tabelle auf eine Eintrags-ID zugreift, ist dieser Eintragsbezeichner höchstwahrscheinlich kurzfristig und nicht langfristig.</span><span class="sxs-lookup"><span data-stu-id="1b39b-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="1b39b-148">Mit kurzfristigen Eintrags-IDs können die entsprechenden Objekte nur in der aktuellen MAPI-Sitzung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="1b39b-149">Ein Client kann überprüfen, ob eine Eintrags-ID kurzfristig ist, indem er überprüft, ob alle Flags im ersten Byte des **abFlags** -Members festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1b39b-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="1b39b-150">Einige Eintrags-IDs sind kurzfristig, haben aber langfristige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="1b39b-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="1b39b-151">Eine solche Eintrags-ID verfügt über eine oder mehrere der entsprechenden Flags, die im ersten Byte des **abFlags** -Elements festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1b39b-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="1b39b-152">Eine **Eintrags** -Struktur ähnelt einer [FLATENTRY](flatentry.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1b39b-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="1b39b-153">Es gibt jedoch einige Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="1b39b-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="1b39b-154">Die \*\*\*\* Größe der Eintrags-ID wird von einer Eintragsstruktur nicht gespeichert. eine **FLATENTRY** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1b39b-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="1b39b-155">Eine **Eintrags** -ID speichert die kennzeichendaten und den Rest des Eintrags Bezeichners separat; eine **FLATENTRY** -Struktur speichert die kennzeichendaten mit dem Rest der Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="1b39b-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="1b39b-156">Eine **Eintrags** -Struktur wird als Parameter an die Methoden der [IMAPIProp](imapipropiunknown.md) -Schnittstelle und an die folgenden **OpenEntry** -Methoden übergeben: [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook::](iaddrbook-openentry.md)OpenEntry, [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession::](imapisession-openentry.md)OpenEntry, [IMAPISupport::](imapisupport-openentry.md)OpenEntry, [IMsgStore::](imsgstore-openentry.md)OpenEntry, [IMSLogon::](imslogon-openentry.md) OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1b39b-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="1b39b-157">Eine **Eintrags** Struktur wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1b39b-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="1b39b-158">Eine **FLATENTRY** -Struktur wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder in einem Stream von Bytes zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="1b39b-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="1b39b-159">Clients sollten immer in natürlich ausgerichteten Eintrags Bezeichnern bestehen.</span><span class="sxs-lookup"><span data-stu-id="1b39b-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="1b39b-160">Obwohl Anbieter willkürlich ausgerichtete Eintrags-IDs behandeln sollten, sollten Clients dieses Verhalten nicht erwarten.</span><span class="sxs-lookup"><span data-stu-id="1b39b-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="1b39b-161">Fehler bei der Übergabe einer gut ausgerichteten Eintrags-ID an eine Methode können einen Ausrichtungsfehler auf RISC-Prozessoren verursachen.</span><span class="sxs-lookup"><span data-stu-id="1b39b-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="1b39b-162">Der natürliche Ausrichtungs Faktor (in der Regel 8 Byte) ist der größte von der CPU unterstützte Datentyp und in der Regel derselbe Ausrichtungs Faktor, der von der systemspeicherzuweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b39b-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="1b39b-163">Eine natürlich ausgerichtete Speicheradresse ermöglicht der CPU den Zugriff auf jeden Datentyp, der an dieser Adresse unterstützt wird, ohne einen Ausrichtungsfehler zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1b39b-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="1b39b-164">Bei RISC-CPUs muss ein Datentyp der Größe N Byte in der Regel auf einem geraden Vielfachen von N Bytes ausgerichtet werden, wobei die Adresse ein gerades Vielfaches von N ist.</span><span class="sxs-lookup"><span data-stu-id="1b39b-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="1b39b-165">Weitere Informationen finden Sie unter [Entry Identifiers](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="1b39b-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b39b-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b39b-166">See also</span></span>



[<span data-ttu-id="1b39b-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="1b39b-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="1b39b-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1b39b-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="1b39b-169">Kanonische Pidtagrecordkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1b39b-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="1b39b-170">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1b39b-170">MAPI Structures</span></span>](mapi-structures.md)

