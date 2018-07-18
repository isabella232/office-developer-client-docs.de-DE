---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792605"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="0308c-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="0308c-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="0308c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0308c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0308c-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0308c-105">Deprecated.</span></span> <span data-ttu-id="0308c-106">Weist einen neuen Namen zu einem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="0308c-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="0308c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0308c-107">Parameters</span></span>

 <span data-ttu-id="0308c-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0308c-108">_lpUID_</span></span>
  
> <span data-ttu-id="0308c-109">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst zum Umbenennen enthält.</span><span class="sxs-lookup"><span data-stu-id="0308c-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="0308c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0308c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0308c-111">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="0308c-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0308c-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="0308c-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="0308c-113">[in] Ein Zeiger auf den neuen Namen für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0308c-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0308c-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0308c-114">Return value</span></span>

<span data-ttu-id="0308c-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0308c-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0308c-116">Dieser Nachrichtendienst umbenennen unterstützt MAPI nicht.</span><span class="sxs-lookup"><span data-stu-id="0308c-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="0308c-117">Dieser Wert wird immer **RenameMsgService** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0308c-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0308c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0308c-118">Remarks</span></span>

<span data-ttu-id="0308c-119">Um eine Message Service einen neuen Namen zuzuweisen, sollten Clients die **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))-Eigenschaft des Diensts Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="0308c-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="0308c-120">Die Namen der Dienstanbieter in einem Nachrichtendienst werden in deren Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0308c-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0308c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0308c-121">See also</span></span>



[<span data-ttu-id="0308c-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0308c-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0308c-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0308c-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

