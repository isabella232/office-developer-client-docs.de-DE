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
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791812"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="d0807-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="d0807-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="d0807-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0807-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0807-105">Gibt an, ob der Exchange-Cache-Modus für den Ordner **Öffentliche Ordner-Favoriten** aktiviert ist, und gibt an, ob dies durch Richtlinien erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="d0807-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d0807-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d0807-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0807-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="d0807-107">Exported by:</span></span>  <br/> |<span data-ttu-id="d0807-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="d0807-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="d0807-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d0807-109">Called by:</span></span>  <br/> |<span data-ttu-id="d0807-110">Client</span><span class="sxs-lookup"><span data-stu-id="d0807-110">Client</span></span>  <br/> |
|<span data-ttu-id="d0807-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d0807-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0807-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="d0807-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="d0807-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0807-113">Parameters</span></span>

 <span data-ttu-id="d0807-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="d0807-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="d0807-115">[out] **true,** Wenn der Rückgabewert ist dies nicht durch Richtlinien, **false** erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="d0807-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d0807-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d0807-116">Return values</span></span>

 <span data-ttu-id="d0807-117">**"true"**</span><span class="sxs-lookup"><span data-stu-id="d0807-117">**true**</span></span>
  
- <span data-ttu-id="d0807-118">Das Zwischenspeichern ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0807-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="d0807-119">**false**</span><span class="sxs-lookup"><span data-stu-id="d0807-119">**false**</span></span>
  
- <span data-ttu-id="d0807-120">Zwischenspeichern ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0807-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0807-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0807-121">See also</span></span>



[<span data-ttu-id="d0807-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="d0807-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

