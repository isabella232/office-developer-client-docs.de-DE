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
ms.openlocfilehash: 7d01f07b5eb5ca34b4bd825b62b7d1520b853d6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564262"
---
# <a name="olfi"></a><span data-ttu-id="3ec5e-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="3ec5e-103">OLFI</span></span>

  
  
<span data-ttu-id="3ec5e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec5e-105">Warteschlange der langfristigen ID Strukturen verwendet durch den Anbieter für Persönliche Ordner-Datei (PST) anmelden, eine Eintrags-ID für eine neue Nachricht oder einen Ordner im Offlinemodus zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3ec5e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="3ec5e-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="3ec5e-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="3ec5e-107">Members</span></span>

 <span data-ttu-id="3ec5e-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-108">_ulVersion_</span></span>
  
- <span data-ttu-id="3ec5e-109">Die Versionsnummer für die Struktur.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="3ec5e-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-110">_muidReserved_</span></span>
  
- <span data-ttu-id="3ec5e-111">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3ec5e-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-112">_ulReserved_</span></span>
  
- <span data-ttu-id="3ec5e-113">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3ec5e-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="3ec5e-115">Die Anzahl der Einträge, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="3ec5e-116">Diese Einträge freigeben denselben global eindeutigen Bezeichner (GUID).</span><span class="sxs-lookup"><span data-stu-id="3ec5e-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="3ec5e-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="3ec5e-118">Die Anzahl der Einträge, die als Nächstes für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="3ec5e-119">Diese Einträge Teilen dieselbe GUID.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="3ec5e-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="3ec5e-121">Langfristige Struktur der-ID, **[LTID](ltid.md)**, der derzeit für die Zuweisung Posten identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="3ec5e-122">Die langfristige ID-Datenstruktur enthält eine GUID und einen Index, die ein Objekt im Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="3ec5e-123">Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="3ec5e-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="3ec5e-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="3ec5e-125">Struktur der langfristigen-ID, die den nächsten verfügbaren Eintrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ec5e-126">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3ec5e-126">Remarks</span></span>

<span data-ttu-id="3ec5e-127">Eine Eintrags-ID ist eine 4-Byte-MAPI-Eintrags-ID für einen Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="3ec5e-128">Weitere Informationen finden Sie unter [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="3ec5e-128">For more information, see [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span></span>
  
<span data-ttu-id="3ec5e-129">Wenn ein neues Objekt durch eine PST-Speicheranbieter eine Eintrags-ID zugewiesen wird, benötigt es zunächst eine GUID, die den Server identifiziert und ein Index, der das Objekt im Speicher angibt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="3ec5e-130">Obwohl die GUID über alle EntryIDs nicht eindeutig ist, geben Sie die GUID und der Index kombiniert einen eindeutigen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="3ec5e-131">Dieses Paar-GUID und der Index nachverfolgt wird durch eine langfristige ID-Struktur **LTID**, das Teil der Struktur **OLFI** ist.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="3ec5e-132">Der PST-Speicher-Anbieter ist nicht physisch im **OLFI** eine **LTID** -Struktur für jedes Paar GUID-Index aufbewahrt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="3ec5e-133">Es bleibt einer **LTID** Struktur *LtidAlloc* für das derzeit erste verfügbaren GUID-Index-Paar. Count, *DwAlloc* die Anzahl der verfügbaren Einträge, die in derselben GUID freigeben; und eine zweite **LTID** -Struktur *LtidNextAlloc* für das nächste verfügbare GUID-Index-Paar, die eine andere GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="3ec5e-134">Die PST-Datei speichert Provider verwendet die Struktur der **OLFI** zum Nachverfolgen der GUIDs und der Indizes, die es, werden ausgegeben hat. Virtuelle Ebene verwaltet der Anbieter eine Reserve einer Zahl von **LTID** -Strukturen, die bereit sind, zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="3ec5e-135">*DwAlloc* hält eine der verfügbaren **LTID** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="3ec5e-136">Anforderungen für die Eintrags-IDs werden blockiert.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="3ec5e-137">Wenn eine Anforderung für einen Block vorhanden ist, überprüft der PST-Speicher-Anbieter befindet sich über ausreichende Reserve verfügbar durch die angeforderte Größe mit *DwAlloc* vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="3ec5e-138">Wenn über ausreichende Reserve vorhanden ist, gibt die GUID und der Index in *LtidAlloc* für die Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="3ec5e-139">Klicken Sie dann verringert *DwAlloc* um die angeforderte Größe und erhöht den Index in *LtidAlloc* um die erforderliche Größe.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="3ec5e-140">Den PST-Speicheranbieter *LtidAlloc* bei der nächsten Anforderung für eine andere Block mit EntryIDs zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="3ec5e-141">Beachten Sie, dass die GUID für die nächste Anforderung unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="3ec5e-142">Wenn die Größe einer Anforderung *DwAlloc* übersteigt, versucht der PST-Speicher-Anbieter verwenden, was sie als Nächstes behalten Sie gemäß *DwNextAlloc* und *LtidNextAlloc* hat.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="3ec5e-143">Es kopiert *DwNextAlloc* und *LtidNextAlloc* *DwAlloc* und *LtidAlloc* und *DwNextAlloc* und *LtidNextAlloc* auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="3ec5e-144">Ein Anbieter, der umbrochen den PST-Speicher-Anbieter wird überprüfen regelmäßig *LtidNextAlloc* , um festzustellen, ob er NULL ist.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="3ec5e-145">Wenn dies der Fall, sollte der Anbieter füllen Sie sie mit einer neuen GUID und *DwNextAlloc* zurückgesetzt, sodass weitere Eintrags-IDs zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ec5e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ec5e-146">See also</span></span>



[<span data-ttu-id="3ec5e-147">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="3ec5e-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3ec5e-148">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="3ec5e-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3ec5e-149">LTID</span><span class="sxs-lookup"><span data-stu-id="3ec5e-149">LTID</span></span>](ltid.md)

