---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0a34c441a473154a43a107b4236ccc259d327dba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348055"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="dffe0-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="dffe0-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="dffe0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dffe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="dffe0-105">Erstellt ein MAPI-Offlineobjekt, das vom Anbieter und Speicher verwendet wird, um MAPI zu benachrichtigen, wenn das Objekt Online und offline geschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="dffe0-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dffe0-106">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="dffe0-106">Exported by:</span></span>  <br/> |<span data-ttu-id="dffe0-107">Msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="dffe0-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="dffe0-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dffe0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dffe0-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="dffe0-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="dffe0-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dffe0-110">Called by:</span></span>  <br/> |<span data-ttu-id="dffe0-111">Client</span><span class="sxs-lookup"><span data-stu-id="dffe0-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="dffe0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dffe0-112">Parameters</span></span>

<span data-ttu-id="dffe0-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dffe0-113">_ulFlags_</span></span>
  
> <span data-ttu-id="dffe0-114">in Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="dffe0-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="dffe0-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="dffe0-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="dffe0-116">in Ein Zeiger auf eine **MAPIOFFLINE_CREATEINFO** -Struktur, die die zum Erstellen des Offline Objekts erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="dffe0-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="dffe0-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="dffe0-117">_ppOffline_</span></span>
  
> <span data-ttu-id="dffe0-118">Out Ein Zeiger auf die **IMAPIOfflineMgr** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dffe0-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dffe0-119">Return value</span><span class="sxs-lookup"><span data-stu-id="dffe0-119">Return value</span></span>

<span data-ttu-id="dffe0-120">None.</span><span class="sxs-lookup"><span data-stu-id="dffe0-120">None.</span></span>
  
<span data-ttu-id="dffe0-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="dffe0-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="dffe0-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dffe0-122">Example</span></span>

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a><span data-ttu-id="dffe0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dffe0-123">See also</span></span>

- [<span data-ttu-id="dffe0-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="dffe0-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="dffe0-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="dffe0-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

