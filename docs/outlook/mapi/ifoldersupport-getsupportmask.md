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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567853"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="3be03-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="3be03-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="3be03-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3be03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3be03-105">Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="3be03-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="3be03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3be03-106">Parameters</span></span>

 <span data-ttu-id="3be03-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="3be03-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="3be03-108">[out] Gibt an, ob der Ordner Freigabe unterstützt eine Bitmaske dar.</span><span class="sxs-lookup"><span data-stu-id="3be03-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="3be03-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="3be03-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="3be03-110">Gibt an, dass der Ordner Freigabe nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3be03-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="3be03-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="3be03-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="3be03-112">Gibt an, dass der Ordner Freigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3be03-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3be03-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3be03-113">Return value</span></span>

<span data-ttu-id="3be03-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3be03-114">S_OK</span></span> 
  
> <span data-ttu-id="3be03-115">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3be03-115">The call was successful.</span></span>
    

