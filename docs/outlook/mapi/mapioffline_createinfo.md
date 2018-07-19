---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793134"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="68e28-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="68e28-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="68e28-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68e28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68e28-105">Diese Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="68e28-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a><span data-ttu-id="68e28-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="68e28-106">Members</span></span>

 <span data-ttu-id="68e28-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="68e28-107">**ulSize**</span></span>
  
> <span data-ttu-id="68e28-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="68e28-108">The size of structure.</span></span>
    
 <span data-ttu-id="68e28-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="68e28-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="68e28-110">Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="68e28-110">It must be 0.</span></span>
    
 <span data-ttu-id="68e28-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="68e28-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="68e28-112">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="68e28-112">The name of the profile.</span></span>
    
 <span data-ttu-id="68e28-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="68e28-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="68e28-114">Eine Bitmaske der folgenden Funktion Flags.</span><span class="sxs-lookup"><span data-stu-id="68e28-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="68e28-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="68e28-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="68e28-116">Das offline-Objekt kann Wechsel in den Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="68e28-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="68e28-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="68e28-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="68e28-118">Das offline-Objekt kann den Onlinemodus wechseln.</span><span class="sxs-lookup"><span data-stu-id="68e28-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="68e28-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="68e28-119">**pGUID**</span></span>
  
> <span data-ttu-id="68e28-120">Zeiger auf eine GUID, die verwendet wird, um diese Art von offline-Objekt aus anderen offline-Objekten eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="68e28-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="68e28-121">GUID_GlobalState bezieht sich auf das globale offline-Objekt, das als ein übergeordnetes Objekt Objekte verwenden können.</span><span class="sxs-lookup"><span data-stu-id="68e28-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="68e28-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="68e28-122">**pInstance**</span></span>
  
> <span data-ttu-id="68e28-123">Zeiger auf die GUID, die dieses offline-Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68e28-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="68e28-124">Es wird verwendet, um diese offline Objekte aus anderen Objekten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="68e28-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="68e28-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="68e28-125">**pParent**</span></span>
  
> <span data-ttu-id="68e28-126">Zeiger auf offline-Objekt, das das übergeordnete Element dieses Objekt offline und deren ist dieses offline-Objekt erbt die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="68e28-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="68e28-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="68e28-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="68e28-128">Gibt das MAPI-Support-Objekt, die dieses offline-Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68e28-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="68e28-129">Wenn dieses Objekt offline um eines Speichers an offline verwendet wird und Onlinestatus, dies wird unterstützt die Speicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="68e28-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="68e28-130">Jedoch ist dies ein offline-Objekt für ein Objekt ohne Unterstützung-Objekt kann es NULL sein.</span><span class="sxs-lookup"><span data-stu-id="68e28-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="68e28-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="68e28-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="68e28-132">Ein Zeiger auf eine MAPIOFFLINE_AGGREGATEINFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="68e28-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="68e28-133">Weitere Informationen finden Sie unter [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="68e28-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="68e28-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="68e28-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="68e28-135">Muss null sein.</span><span class="sxs-lookup"><span data-stu-id="68e28-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68e28-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68e28-136">See also</span></span>



[<span data-ttu-id="68e28-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="68e28-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="68e28-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="68e28-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

