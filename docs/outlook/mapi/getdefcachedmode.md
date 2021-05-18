---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412744"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="1a166-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="1a166-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="1a166-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a166-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a166-105">Gibt an, ob Exchange für den privaten Exchange aktiviert ist und ob dies durch die Richtlinie erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="1a166-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1a166-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1a166-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a166-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="1a166-107">Exported by:</span></span>  <br/> |<span data-ttu-id="1a166-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="1a166-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="1a166-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1a166-109">Called by:</span></span>  <br/> |<span data-ttu-id="1a166-110">Client</span><span class="sxs-lookup"><span data-stu-id="1a166-110">Client</span></span>  <br/> |
|<span data-ttu-id="1a166-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1a166-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a166-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="1a166-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="1a166-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a166-113">Parameters</span></span>

 <span data-ttu-id="1a166-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="1a166-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="1a166-115">[out] **true,** wenn der Rückgabewert von der Richtlinie erzwungen wird, **false,** wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="1a166-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1a166-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1a166-116">Return values</span></span>

 <span data-ttu-id="1a166-117">**true**</span><span class="sxs-lookup"><span data-stu-id="1a166-117">**true**</span></span>
  
- <span data-ttu-id="1a166-118">Die Zwischenspeicherung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a166-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="1a166-119">**false**</span><span class="sxs-lookup"><span data-stu-id="1a166-119">**false**</span></span>
  
- <span data-ttu-id="1a166-120">Die Zwischenspeicherung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a166-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a166-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a166-121">See also</span></span>



[<span data-ttu-id="1a166-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="1a166-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

