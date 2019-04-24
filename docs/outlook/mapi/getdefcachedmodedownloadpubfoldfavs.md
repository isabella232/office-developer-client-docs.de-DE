---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299888"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="83375-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="83375-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="83375-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83375-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83375-105">Gibt an, ob der Exchange-Cache-Modus für den Ordner **Favoriten für Öffentliche Ordner** aktiviert ist und ob dieser durch die Richtlinie erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="83375-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="83375-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="83375-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83375-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="83375-107">Exported by:</span></span>  <br/> |<span data-ttu-id="83375-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="83375-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="83375-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="83375-109">Called by:</span></span>  <br/> |<span data-ttu-id="83375-110">Client</span><span class="sxs-lookup"><span data-stu-id="83375-110">Client</span></span>  <br/> |
|<span data-ttu-id="83375-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="83375-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="83375-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="83375-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="83375-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="83375-113">Parameters</span></span>

 <span data-ttu-id="83375-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="83375-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="83375-115">Out **true** , wenn der Rückgabewert durch die Richtlinie erzwungen wird, **false** , wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="83375-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="83375-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="83375-116">Return values</span></span>

 <span data-ttu-id="83375-117">**true**</span><span class="sxs-lookup"><span data-stu-id="83375-117">**true**</span></span>
  
- <span data-ttu-id="83375-118">Zwischenspeicherung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="83375-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="83375-119">**false**</span><span class="sxs-lookup"><span data-stu-id="83375-119">**false**</span></span>
  
- <span data-ttu-id="83375-120">Zwischenspeicherung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="83375-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83375-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83375-121">See also</span></span>



[<span data-ttu-id="83375-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="83375-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

