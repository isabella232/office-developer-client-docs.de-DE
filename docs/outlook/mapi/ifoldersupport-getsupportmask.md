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
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350834"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="eff9a-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="eff9a-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="eff9a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eff9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eff9a-105">Ruft Informationen über die Unterstützung eines Ordners für die Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="eff9a-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="eff9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eff9a-106">Parameters</span></span>

 <span data-ttu-id="eff9a-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="eff9a-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="eff9a-108">Out Eine Bitmaske, die angibt, ob der Ordnerfreigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eff9a-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="eff9a-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="eff9a-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="eff9a-110">Gibt an, dass der Ordner keine Freigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eff9a-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="eff9a-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="eff9a-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="eff9a-112">Gibt an, dass der Ordnerfreigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eff9a-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eff9a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eff9a-113">Return value</span></span>

<span data-ttu-id="eff9a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="eff9a-114">S_OK</span></span> 
  
> <span data-ttu-id="eff9a-115">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eff9a-115">The call was successful.</span></span>
    

