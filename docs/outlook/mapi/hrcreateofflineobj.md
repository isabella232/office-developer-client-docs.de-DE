---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0a34c441a473154a43a107b4236ccc259d327dba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414389"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="a0120-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="a0120-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="a0120-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0120-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a0120-105">Erstellt ein MAPI-Offlineobjekt, das vom Anbieter und Speicher verwendet wird, um MAPI zu benachrichtigen, wenn das Objekt online und offline geht.</span><span class="sxs-lookup"><span data-stu-id="a0120-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0120-106">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="a0120-106">Exported by:</span></span>  <br/> |<span data-ttu-id="a0120-107">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a0120-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a0120-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a0120-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0120-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="a0120-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="a0120-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a0120-110">Called by:</span></span>  <br/> |<span data-ttu-id="a0120-111">Client</span><span class="sxs-lookup"><span data-stu-id="a0120-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="a0120-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0120-112">Parameters</span></span>

<span data-ttu-id="a0120-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0120-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a0120-114">[in] Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="a0120-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="a0120-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="a0120-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="a0120-116">[in] Ein Zeiger auf eine **MAPIOFFLINE_CREATEINFO,** die die informationen enthält, die zum Erstellen des Offlineobjekts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a0120-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="a0120-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="a0120-117">_ppOffline_</span></span>
  
> <span data-ttu-id="a0120-118">[out] Ein Zeiger auf die **IMAPIOfflineMgr-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="a0120-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0120-119">Return value</span><span class="sxs-lookup"><span data-stu-id="a0120-119">Return value</span></span>

<span data-ttu-id="a0120-120">None.</span><span class="sxs-lookup"><span data-stu-id="a0120-120">None.</span></span>
  
<span data-ttu-id="a0120-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="a0120-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="a0120-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0120-122">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a0120-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0120-123">See also</span></span>

- [<span data-ttu-id="a0120-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="a0120-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="a0120-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="a0120-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

