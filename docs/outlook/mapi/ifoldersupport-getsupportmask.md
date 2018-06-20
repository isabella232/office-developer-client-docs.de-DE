---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792059"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="7cc11-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="7cc11-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="7cc11-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cc11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cc11-105">Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="7cc11-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="7cc11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cc11-106">Parameters</span></span>

 <span data-ttu-id="7cc11-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="7cc11-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="7cc11-108">[out] Gibt an, ob der Ordner Freigabe unterstützt eine Bitmaske dar.</span><span class="sxs-lookup"><span data-stu-id="7cc11-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="7cc11-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="7cc11-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="7cc11-110">Gibt an, dass der Ordner Freigabe nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7cc11-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="7cc11-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="7cc11-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="7cc11-112">Gibt an, dass der Ordner Freigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7cc11-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7cc11-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7cc11-113">Return value</span></span>

<span data-ttu-id="7cc11-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cc11-114">S_OK</span></span> 
  
> <span data-ttu-id="7cc11-115">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7cc11-115">The call was successful.</span></span>
    

