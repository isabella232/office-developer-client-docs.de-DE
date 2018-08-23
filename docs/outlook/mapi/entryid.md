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
ms.openlocfilehash: 8540176b7675917dde7c618c40142605e9622282
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586221"
---
# <a name="entryid"></a><span data-ttu-id="60959-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="60959-103">ENTRYID</span></span>

  
  
<span data-ttu-id="60959-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60959-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60959-105">Enthält einen Eintrag Bezeichner für ein MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="60959-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60959-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="60959-106">Header file:</span></span>  <br/> |<span data-ttu-id="60959-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60959-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="60959-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="60959-108">Related macros:</span></span>  <br/> |<span data-ttu-id="60959-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="60959-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="60959-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="60959-110">Members</span></span>

 <span data-ttu-id="60959-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="60959-111">**abFlags**</span></span>
  
> <span data-ttu-id="60959-112">Bitmaske aus Flags, die Informationen enthalten, die das Objekt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60959-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="60959-113">Vom Anbieter kann nur auf das erste Byte des die Kennzeichen, **AbFlags [0]**, festgelegt werden. die anderen drei sind vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="60959-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="60959-114">Diese Flags müssen für permanente-Eintragsbezeichner nicht festgelegt werden. Sie sind nur für kurzfristige-Eintragsbezeichner festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60959-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="60959-115">Clients ist diese Struktur schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="60959-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="60959-116">Die folgenden Kennzeichen können in **AbFlags [0]** festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="60959-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="60959-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="60959-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="60959-118">Die Eintrags-ID kann nicht als Empfänger einer Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60959-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="60959-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="60959-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="60959-120">Andere Benutzer können nicht die Eintrags-ID zugreifen.</span><span class="sxs-lookup"><span data-stu-id="60959-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="60959-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="60959-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="60959-122">Die Eintrags-ID kann nicht in anderen Fällen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60959-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="60959-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="60959-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="60959-124">Die Eintrags-ID ist kurzfristige.</span><span class="sxs-lookup"><span data-stu-id="60959-124">The entry identifier is short-term.</span></span> <span data-ttu-id="60959-125">Alle anderen Werte in Byte müssen festgelegt werden, es sei denn, weitere Verwendungsmöglichkeiten des Bezeichners Eintrag aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="60959-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="60959-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="60959-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="60959-127">Die Eintrags-ID kann nicht auf andere-Sitzungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60959-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="60959-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="60959-128">**ab**</span></span>
  
> <span data-ttu-id="60959-129">Gibt ein Array von binären Daten, die vom Dienstanbieter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60959-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="60959-130">Die Client-Anwendung kann nicht in Array verwenden.</span><span class="sxs-lookup"><span data-stu-id="60959-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60959-131">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="60959-131">Remarks</span></span>

<span data-ttu-id="60959-132">Die **ENTRYID** -Struktur wird von der Nachricht speichern und Beheben von adressbuchanbietern implementierte zum Erstellen von eindeutiger Bezeichnern für Objekte.</span><span class="sxs-lookup"><span data-stu-id="60959-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="60959-133">Eintragsbezeichner werden verwendet, um die folgenden Typen von Objekten zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="60959-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="60959-134">Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="60959-134">Message stores</span></span>
    
- <span data-ttu-id="60959-135">Ordner</span><span class="sxs-lookup"><span data-stu-id="60959-135">Folders</span></span>
    
- <span data-ttu-id="60959-136">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="60959-136">Messages</span></span>
    
- <span data-ttu-id="60959-137">Address Book Container</span><span class="sxs-lookup"><span data-stu-id="60959-137">Address book containers</span></span>
    
- <span data-ttu-id="60959-138">Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="60959-138">Distribution lists</span></span>
    
- <span data-ttu-id="60959-139">Messaging-Benutzer</span><span class="sxs-lookup"><span data-stu-id="60959-139">Messaging users</span></span>
    
- <span data-ttu-id="60959-140">Status-Objekte</span><span class="sxs-lookup"><span data-stu-id="60959-140">Status objects</span></span>
    
- <span data-ttu-id="60959-141">Profil Abschnitte</span><span class="sxs-lookup"><span data-stu-id="60959-141">Profile sections</span></span>
    
<span data-ttu-id="60959-142">Jeder Provider verwendet ein Format für die **Eintrags-ID** -Struktur, die für diesen Anbieter sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="60959-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="60959-143">Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="60959-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="60959-144">Um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen, rufen Sie die [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="60959-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="60959-145">Wenn ein Client ein Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um die Eintrags-ID abrufen aufruft, gibt das Objekt am häufigsten permanente Form eines Eintrags-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="60959-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="60959-146">Ein Client überprüfen, ob eine Eintrags-ID langfristige ist, indem Sie überprüfen, dass keines der Flags im ersten Byte des Elements **AbFlags** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="60959-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="60959-147">Wenn ein Client greift auf eine Eintrags-ID über eine Spalte in einer Tabelle, die dieses Eintrags-ID anstelle von langfristige kurzfristige ist wahrscheinlich.</span><span class="sxs-lookup"><span data-stu-id="60959-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="60959-148">Kurzfristige-Eintragsbezeichner können verwendet werden, um die entsprechenden Objekte nur in der aktuellen MAPI-Sitzung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="60959-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="60959-149">Ein Client überprüfen, ob eine Eintrags-ID kurzfristige ist, indem Sie überprüfen, dass alle Kennzeichen im ersten Byte des Elements **AbFlags** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="60959-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="60959-150">Einige Eintragsbezeichner sind kurzfristig, aber langfristige verwenden.</span><span class="sxs-lookup"><span data-stu-id="60959-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="60959-151">Solche Eintrags-ID wird mindestens eines der entsprechenden Flags, die in dem ersten Byte des **AbFlags** Mitglied festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="60959-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="60959-152">Eine Struktur **ENTRYID** ähnelt eine [FLATENTRY](flatentry.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="60959-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="60959-153">Es gibt jedoch einige Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="60959-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="60959-154">Eine **ENTRYID** -Struktur wird die Größe des Eintrags-ID nicht gespeichert; Es wird eine **FLATENTRY** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="60959-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="60959-155">Eine Struktur **ENTRYID** speichert die Flag-Daten und den Rest des Bezeichners Eintrag separat; eine Struktur **FLATENTRY** speichert die Kennzeichnungsdaten mit dem Rest der Eintrags-ID an.</span><span class="sxs-lookup"><span data-stu-id="60959-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="60959-156">Eine **ENTRYID** -Struktur wird als Parameter übergeben, an die Methoden der Schnittstelle [IMAPIProp](imapipropiunknown.md) und auf die folgenden Methoden **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="60959-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="60959-157">Eine **ENTRYID** -Struktur wird verwendet, um die Eintrags-ID auf dem Datenträger speichern.</span><span class="sxs-lookup"><span data-stu-id="60959-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="60959-158">Eine Struktur **FLATENTRY** wird verwendet, um eine Eintrags-ID in einer Datei speichern, oder geben Sie ihn in einen Datenstrom von Bytes.</span><span class="sxs-lookup"><span data-stu-id="60959-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="60959-159">Clients sollte immer natürlich ausgerichtet-Eintragsbezeichner übergeben.</span><span class="sxs-lookup"><span data-stu-id="60959-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="60959-160">Obwohl Anbieter willkürlich ausgerichtete-Eintragsbezeichner behandelt werden sollen, sollten Clients dieses Verhalten nicht erwarten.</span><span class="sxs-lookup"><span data-stu-id="60959-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="60959-161">Eine gute ausgerichtete Eintrags-ID an eine Methode übergeben können Ausrichtungsfehler durch eine auf RISC-Prozessoren führen.</span><span class="sxs-lookup"><span data-stu-id="60959-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="60959-162">Der natürlichen Ausrichtung Faktor, in der Regel 8 Byte ist der größte Datentyp, der von der CPU unterstützt und in der Regel den gleichen Ausrichtung Faktor durch das System Arbeitsspeicher Zuweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="60959-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="60959-163">Eine Adresse natürlich ausgerichteten Speicher ermöglicht die CPU auf einen beliebigen Datentyp zugreifen, die sie an dieser Adresse unterstützt ohne Ausrichtungsfehler durch eine generieren.</span><span class="sxs-lookup"><span data-stu-id="60959-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="60959-164">Für RISC CPUs muss ein Datentyp der Größe N Bytes in der Regel auf kein Vielfaches von N Bytes, mit der Adresse wird kein Vielfaches von n ausgerichtet werden</span><span class="sxs-lookup"><span data-stu-id="60959-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="60959-165">Weitere Informationen finden Sie unter [Eintragsbezeichner](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="60959-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60959-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60959-166">See also</span></span>



[<span data-ttu-id="60959-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="60959-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="60959-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="60959-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="60959-169">PidTagRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="60959-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="60959-170">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="60959-170">MAPI Structures</span></span>](mapi-structures.md)

