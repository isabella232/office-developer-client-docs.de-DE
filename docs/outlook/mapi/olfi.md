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
# <a name="olfi"></a><span data-ttu-id="e8a0c-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="e8a0c-103">OLFI</span></span>

  
  
<span data-ttu-id="e8a0c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8a0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8a0c-105">Warteschlange für langfristige ID-Strukturen, die vom Speicheranbieter für persönliche Ordner-Dateien (PST) verwendet werden, um eine Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e8a0c-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e8a0c-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e8a0c-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="e8a0c-107">Members</span></span>

 <span data-ttu-id="e8a0c-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-108">_ulVersion_</span></span>
  
- <span data-ttu-id="e8a0c-109">Versionsnummer für die Struktur.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="e8a0c-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-110">_muidReserved_</span></span>
  
- <span data-ttu-id="e8a0c-111">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="e8a0c-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-112">_ulReserved_</span></span>
  
- <span data-ttu-id="e8a0c-113">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="e8a0c-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="e8a0c-115">Die Anzahl der Einträge, die für die Zuordnung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="e8a0c-116">Diese Einträge haben dieselbe GUID (Globally Unique Identifier).</span><span class="sxs-lookup"><span data-stu-id="e8a0c-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="e8a0c-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="e8a0c-118">Die Anzahl der Einträge, die als nächstes für die Zuordnung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="e8a0c-119">Diese Einträge haben dieselbe GUID.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="e8a0c-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="e8a0c-121">Die langfristige ID-Struktur, **[LTID](ltid.md)**, die den derzeit für die Zuordnung verfügbaren Eintrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="e8a0c-122">Die langfristige ID-Struktur enthält eine GUID und einen Index, der ein Objekt im Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="e8a0c-123">Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="e8a0c-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="e8a0c-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="e8a0c-125">Langfristige ID-Struktur, die den nächsten verfügbaren Eintrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8a0c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8a0c-126">Remarks</span></span>

<span data-ttu-id="e8a0c-127">Eine Eintrags-ID ist ein 4-Byte-MAPI-Eintragsbezeichner für einen Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="e8a0c-128">Weitere Informationen finden Sie unter [Eintrags](https://msdn.microsoft.com/library/ms836424)-Nr.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="e8a0c-129">Wenn ein PST-Speicheranbieter einem neuen Objekt eine Eintrags-ID zuweist, benötigt er zunächst eine GUID, die den Server identifiziert, und einen Index, der das Objekt im Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="e8a0c-130">Obwohl die GUID für alle Eintrags-IDs nicht eindeutig ist, bieten die GUID und der kombinierte Index einen eindeutigen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="e8a0c-131">Dieses GUID-und Index-Paar wird durch eine langfristige ID-Struktur, **LTID**, nachverfolgt, die Teil der **OLFI** -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="e8a0c-132">Der PST-Speicheranbieter hält in **OLFI** für jedes GUID-Index-paar keine **LTID** -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="e8a0c-133">Es behält eine **LTID** -Struktur, *ltidAlloc* , für das derzeit erste verfügbare GUID-Index-paar; count, *dwAlloc* , der Anzahl der verfügbaren Einträge, die dieselbe GUID verwenden; und eine zweite **LTID** -Struktur, *ltidNextAlloc* , für das nächste verfügbare GUID-Index-Paar mit einer anderen GUID.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="e8a0c-134">Der PST-Speicheranbieter verwendet die **OLFI** -Struktur, um die überLIEFERTen GUIDs und Indizes nachzuverfolgen. Auf einer virtuellen Ebene verwaltet der Anbieter eine Reserve für eine Reihe von **LTID** -Strukturen, die bereit für die Zuordnung sind.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="e8a0c-135">*dwAlloc* verwaltet die Anzahl der verfügbaren **LTID** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="e8a0c-136">Anforderungen für Eintrags-IDs werden in Blöcken gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="e8a0c-137">Wenn es eine Anforderung für einen Block gibt, überprüft der PST-Speicheranbieter, ob ausreichend Reserve vorhanden ist, indem die angeforderte Größe mit *dwAlloc* verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="e8a0c-138">Wenn genügend Reserve vorhanden ist, werden die GUID und der Index in *ltidAlloc* für die Zuordnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="e8a0c-139">Anschließend wird *dwAlloc* um die angeforderte Größe verringert und der Index in *ltidAlloc* um die angeforderte Größe erhöht.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="e8a0c-140">Dadurch wird der PST-Speicheranbieter darauf vorbereitet, *ltidAlloc* für die nächste Anforderung für einen weiteren Block von Eintrags-IDs zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="e8a0c-141">Beachten Sie, dass die GUID für die nächste Anforderung identisch bleibt.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="e8a0c-142">Wenn die Größe einer Anforderung größer als *dwAlloc* ist, versucht der PST-Speicheranbieter zu verwenden, was er als nächstes in Reserve hat, wie von *dwNextAlloc* und *ltidNextAlloc* angegeben.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="e8a0c-143">*DwNextAlloc* und *LtidNextAlloc* werden in *dwAlloc* und *ltidAlloc* kopiert, und *dwNextAlloc* und *ltidNextAlloc* werden auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="e8a0c-144">Ein Anbieter, der den PST-Speicheranbieter umschließt, sollte *ltidNextAlloc* in regelmäßigen Abständen überprüfen, ob er NULL ist.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="e8a0c-145">Wenn dies der Fall ist, sollte der Anbieter es mit einer neuen GUID auffüllen und *dwNextAlloc* zurücksetzen, damit mehr Eintrags-IDs zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="e8a0c-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8a0c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8a0c-146">See also</span></span>



[<span data-ttu-id="e8a0c-147">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="e8a0c-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e8a0c-148">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="e8a0c-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e8a0c-149">LTID</span><span class="sxs-lookup"><span data-stu-id="e8a0c-149">LTID</span></span>](ltid.md)

