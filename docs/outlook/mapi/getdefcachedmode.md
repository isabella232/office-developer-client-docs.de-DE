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
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591394"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="2f101-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="2f101-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="2f101-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f101-105">Gibt an, ob der Exchange-Cache-Modus für private Exchange-Speicher aktiviert ist, und gibt an, ob dies durch Richtlinien erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="2f101-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2f101-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2f101-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f101-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="2f101-107">Exported by:</span></span>  <br/> |<span data-ttu-id="2f101-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="2f101-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2f101-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2f101-109">Called by:</span></span>  <br/> |<span data-ttu-id="2f101-110">Client</span><span class="sxs-lookup"><span data-stu-id="2f101-110">Client</span></span>  <br/> |
|<span data-ttu-id="2f101-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2f101-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f101-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="2f101-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="2f101-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f101-113">Parameters</span></span>

 <span data-ttu-id="2f101-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="2f101-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="2f101-115">[out] **true,** Wenn der Rückgabewert ist dies nicht durch Richtlinien, **false** erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="2f101-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2f101-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2f101-116">Return values</span></span>

 <span data-ttu-id="2f101-117">**true**</span><span class="sxs-lookup"><span data-stu-id="2f101-117">**true**</span></span>
  
- <span data-ttu-id="2f101-118">Das Zwischenspeichern ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f101-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="2f101-119">**false**</span><span class="sxs-lookup"><span data-stu-id="2f101-119">**false**</span></span>
  
- <span data-ttu-id="2f101-120">Zwischenspeichern ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f101-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f101-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f101-121">See also</span></span>



[<span data-ttu-id="2f101-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="2f101-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

