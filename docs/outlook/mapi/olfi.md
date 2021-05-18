---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279753"
---
# <a name="olfi"></a><span data-ttu-id="35d94-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="35d94-103">OLFI</span></span>

  
  
<span data-ttu-id="35d94-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35d94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35d94-105">Warteschlange mit langfristigen ID-Strukturen, die vom Anbieter des Informationsspeichers für persönliche Ordner (Personal Folders File, PST) zum Zuweisen einer Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35d94-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="35d94-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="35d94-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="35d94-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="35d94-107">Members</span></span>

 <span data-ttu-id="35d94-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="35d94-108">_ulVersion_</span></span>
  
- <span data-ttu-id="35d94-109">Versionsnummer für die Struktur.</span><span class="sxs-lookup"><span data-stu-id="35d94-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="35d94-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="35d94-110">_muidReserved_</span></span>
  
- <span data-ttu-id="35d94-111">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35d94-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="35d94-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="35d94-112">_ulReserved_</span></span>
  
- <span data-ttu-id="35d94-113">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35d94-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="35d94-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="35d94-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="35d94-115">Die Anzahl der Einträge, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="35d94-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="35d94-116">Diese Einträge haben dieselbe guiD (Globally Unique Identifier).</span><span class="sxs-lookup"><span data-stu-id="35d94-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="35d94-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="35d94-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="35d94-118">Die Anzahl der Einträge, die als Nächstes für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="35d94-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="35d94-119">Diese Einträge haben dieselbe GUID.</span><span class="sxs-lookup"><span data-stu-id="35d94-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="35d94-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="35d94-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="35d94-121">Die langfristige ID-Struktur **[LTID,](ltid.md)** die den eintrag identifiziert, der derzeit für die Zuweisung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="35d94-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="35d94-122">Die langfristige ID-Struktur enthält eine GUID und einen Index, der ein Objekt im Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35d94-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="35d94-123">Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden.</span><span class="sxs-lookup"><span data-stu-id="35d94-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="35d94-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="35d94-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="35d94-125">Langfristige ID-Struktur, die den nächsten verfügbaren Eintrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35d94-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35d94-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35d94-126">Remarks</span></span>

<span data-ttu-id="35d94-127">Eine Eintrags-ID ist eine 4-Byte-MAPI-Eintrags-ID für einen Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="35d94-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="35d94-128">Weitere Informationen finden Sie unter [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="35d94-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="35d94-129">Wenn ein Pst Store-Anbieter einem neuen Objekt eine Eintrags-ID zu weist, benötigt er zunächst eine GUID, die den Server identifiziert, und einen Index, der das Objekt im Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35d94-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="35d94-130">Auch wenn die GUID nicht für alle Eintrags-IDs eindeutig ist, bieten die GUID und der Index zusammen einen eindeutigen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="35d94-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="35d94-131">Dieses GUID- und Indexpaar wird von einer langfristigen ID-Struktur, **LTID**, nachverfolgt, die Teil der **OLFI-Struktur** ist.</span><span class="sxs-lookup"><span data-stu-id="35d94-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="35d94-132">Der Anbieter des PST-Speichers hält in **OLFI** keine **LTID-Struktur** für jedes GUID-Indexpaar.</span><span class="sxs-lookup"><span data-stu-id="35d94-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="35d94-133">Es behält eine **LTID-Struktur,**  *ltidAlloc*  , für das derzeit erste verfügbare GUID-Index-Paar bei. eine Anzahl,  *dwAlloc*  , der Anzahl der verfügbaren Einträge, die dieselbe GUID gemeinsam verwenden; und eine zweite **LTID-Struktur,**  *ltidNextAlloc*  , für das nächste verfügbare GUID-Indexpaar mit einer anderen GUID.</span><span class="sxs-lookup"><span data-stu-id="35d94-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="35d94-134">Der Anbieter des PST-Speichers verwendet die **OLFI-Struktur,** um die von ihm bereitgestellten GUIDs und Indizes nachzuverfolgen. Auf virtueller Ebene verwaltet der Anbieter eine Reserve einer Reihe von **LTID-Strukturen,** die zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="35d94-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="35d94-135">*dwAlloc* verwaltet eine Anzahl der verfügbaren **LTID-Strukturen.**</span><span class="sxs-lookup"><span data-stu-id="35d94-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="35d94-136">Anforderungen für Eintrags-IDs werden in Blöcken verwendet.</span><span class="sxs-lookup"><span data-stu-id="35d94-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="35d94-137">Wenn eine Anforderung für einen Block vorhanden ist, überprüft der Anbieter des PST-Speichers, ob genügend Reserve verfügbar ist, indem er die angeforderte Größe mit *dwAlloc vergleicht.*</span><span class="sxs-lookup"><span data-stu-id="35d94-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="35d94-138">Wenn genügend Reserve vorhanden ist, werden die GUID und der Index in  *ltidAlloc für die Zuordnung*  zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35d94-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="35d94-139">Anschließend wird  *dwAlloc*  um die angeforderte Größe verringert und der Index in  *ltidAlloc*  um die angeforderte Größe erhöht.</span><span class="sxs-lookup"><span data-stu-id="35d94-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="35d94-140">Dadurch wird der Anbieter des PST-Speichers darauf vorbereitet,  *ltidAlloc bei*  der nächsten Anforderung für einen weiteren Block von Eintrags-IDs zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="35d94-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="35d94-141">Beachten Sie, dass die GUID für die nächste Anforderung unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="35d94-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="35d94-142">Wenn die Größe einer Anforderung größer als  *"dwAlloc"*  ist, versucht der Anbieter des PST-Speichers, das als Nächstes in der Reserve zu verwenden, wie von  *dwNextAlloc*  und  *ltidNextAlloc*  angegeben.</span><span class="sxs-lookup"><span data-stu-id="35d94-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="35d94-143">Sie kopiert  *dwNextAlloc*  und  *ltidNextAlloc*  in  *dwAlloc*  bzw.  *ltidAlloc*  und legt  *dwNextAlloc*  und  *ltidNextAlloc*  auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="35d94-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="35d94-144">Ein Anbieter, der den Anbieter für den PST-Speicher umschließt, sollte in regelmäßigen Abständen  *ltidNextAlloc*  überprüfen, um zu prüfen, ob er NULL ist.</span><span class="sxs-lookup"><span data-stu-id="35d94-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="35d94-145">Falls ja, sollte der Anbieter eine neue GUID auffüllen und  *dwNextAlloc*  zurücksetzen, damit weitere Eintrags-IDs zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="35d94-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35d94-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35d94-146">See also</span></span>



[<span data-ttu-id="35d94-147">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="35d94-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="35d94-148">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="35d94-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="35d94-149">LTID</span><span class="sxs-lookup"><span data-stu-id="35d94-149">LTID</span></span>](ltid.md)

