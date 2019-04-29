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
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429565"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="1a8eb-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="1a8eb-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="1a8eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a8eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a8eb-105">Diese Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="1a8eb-106">Members</span><span class="sxs-lookup"><span data-stu-id="1a8eb-106">Members</span></span>

 <span data-ttu-id="1a8eb-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-107">**ulSize**</span></span>
  
> <span data-ttu-id="1a8eb-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-108">The size of structure.</span></span>
    
 <span data-ttu-id="1a8eb-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="1a8eb-110">Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-110">It must be 0.</span></span>
    
 <span data-ttu-id="1a8eb-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="1a8eb-112">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-112">The name of the profile.</span></span>
    
 <span data-ttu-id="1a8eb-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="1a8eb-114">Eine Bitmaske der folgenden Capability Flags.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="1a8eb-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1a8eb-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="1a8eb-116">Das Offlineobjekt kann offline geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="1a8eb-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1a8eb-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="1a8eb-118">Das Offlineobjekt kann online gehen.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="1a8eb-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-119">**pGUID**</span></span>
  
> <span data-ttu-id="1a8eb-120">Zeiger auf eine GUID, die verwendet wird, um diese Art von Offlineobjekt von anderen Offlineobjekten eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="1a8eb-121">GUID_GlobalState bezieht sich auf das globale Offlineobjekt, das Objekte als übergeordnetes Objekt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="1a8eb-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-122">**pInstance**</span></span>
  
> <span data-ttu-id="1a8eb-123">Zeiger auf GUID, die dieses Offlineobjekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="1a8eb-124">Es wird verwendet, um diese Offlineobjekte von anderen Objekten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="1a8eb-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-125">**pParent**</span></span>
  
> <span data-ttu-id="1a8eb-126">Zeiger auf das Offline-Objekt, das das übergeordnete Element dieses Offline Objekts ist und dessen Änderungen dieses Offlineobjekt erbt.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="1a8eb-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="1a8eb-128">Identifiziert das MAPI-Unterstützungsobjekt, das dieses Offlineobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="1a8eb-129">Wenn beispielsweise dieses Offlineobjekt verwendet wird, um den Offline-und Onlinestatus eines Speichers nachzuverfolgen, handelt es sich um das Support Objekt Stores.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="1a8eb-130">Wenn es sich jedoch um ein Offlineobjekt für ein Objekt ohne Support Objekt handelt, kann es NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="1a8eb-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="1a8eb-132">Ein Zeiger auf eine MAPIOFFLINE_AGGREGATEINFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="1a8eb-133">Weitere Informationen finden Sie unter [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1a8eb-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="1a8eb-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="1a8eb-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="1a8eb-135">Muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1a8eb-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a8eb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a8eb-136">See also</span></span>



[<span data-ttu-id="1a8eb-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="1a8eb-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="1a8eb-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="1a8eb-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

