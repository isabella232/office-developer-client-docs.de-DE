---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417707"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="a1aff-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="a1aff-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="a1aff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1aff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1aff-105">Gibt an, ob der Exchange-Cachemodus für den Ordner "Favoriten für öffentliche Ordner" aktiviert ist und ob **dies** durch die Richtlinie erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="a1aff-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a1aff-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a1aff-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1aff-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="a1aff-107">Exported by:</span></span>  <br/> |<span data-ttu-id="a1aff-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a1aff-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a1aff-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a1aff-109">Called by:</span></span>  <br/> |<span data-ttu-id="a1aff-110">Client</span><span class="sxs-lookup"><span data-stu-id="a1aff-110">Client</span></span>  <br/> |
|<span data-ttu-id="a1aff-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a1aff-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1aff-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="a1aff-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="a1aff-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1aff-113">Parameters</span></span>

 <span data-ttu-id="a1aff-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="a1aff-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="a1aff-115">[out] **true,** wenn der Rückgabewert von der Richtlinie erzwungen wird, **false,** wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="a1aff-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a1aff-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a1aff-116">Return values</span></span>

 <span data-ttu-id="a1aff-117">**true**</span><span class="sxs-lookup"><span data-stu-id="a1aff-117">**true**</span></span>
  
- <span data-ttu-id="a1aff-118">Die Zwischenspeicherung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1aff-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="a1aff-119">**false**</span><span class="sxs-lookup"><span data-stu-id="a1aff-119">**false**</span></span>
  
- <span data-ttu-id="a1aff-120">Die Zwischenspeicherung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1aff-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1aff-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1aff-121">See also</span></span>



[<span data-ttu-id="a1aff-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="a1aff-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

