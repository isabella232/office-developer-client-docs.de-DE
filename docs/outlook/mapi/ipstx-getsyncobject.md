---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792819"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="34943-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="34943-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="34943-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34943-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34943-105">Startet eine Sitzung Synchronisierung und ruft die zugehörige **[IOSTX](iostxiunknown.md)** Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="34943-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="34943-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34943-106">Parameters</span></span>

 <span data-ttu-id="34943-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="34943-107">_ppostx_</span></span>
  
>  <span data-ttu-id="34943-108">[out] Zeiger auf die **IOSTX** -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34943-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34943-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34943-109">Remarks</span></span>

<span data-ttu-id="34943-110">Der Aufrufer muss sicherstellen, dass im gleiche Ordner nicht gleichzeitig auf mehreren Threads synchronisiert ist.</span><span class="sxs-lookup"><span data-stu-id="34943-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34943-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34943-111">See also</span></span>



[<span data-ttu-id="34943-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="34943-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="34943-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="34943-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

