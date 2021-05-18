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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422103"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="a56c3-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="a56c3-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="a56c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a56c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a56c3-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a56c3-105">Deprecated.</span></span> <span data-ttu-id="a56c3-106">Weist einem Nachrichtendienst einen neuen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="a56c3-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="a56c3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56c3-107">Parameters</span></span>

 <span data-ttu-id="a56c3-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="a56c3-108">_lpUID_</span></span>
  
> <span data-ttu-id="a56c3-109">[in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den umzubenennenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="a56c3-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="a56c3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a56c3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a56c3-111">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a56c3-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a56c3-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="a56c3-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="a56c3-113">[in] Ein Zeiger auf den neuen Namen für den Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="a56c3-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a56c3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a56c3-114">Return value</span></span>

<span data-ttu-id="a56c3-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a56c3-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a56c3-116">MapI unterstützt die Umbenennung dieses Nachrichtendiensts nicht.</span><span class="sxs-lookup"><span data-stu-id="a56c3-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="a56c3-117">**RenameMsgService** gibt diesen Wert immer zurück.</span><span class="sxs-lookup"><span data-stu-id="a56c3-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a56c3-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a56c3-118">Remarks</span></span>

<span data-ttu-id="a56c3-119">Um einem Nachrichtendienst einen neuen Namen zuzuordnen, sollten Clients die **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) -Eigenschaft des Nachrichtendiensts verwenden.</span><span class="sxs-lookup"><span data-stu-id="a56c3-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="a56c3-120">Die Namen von Dienstanbietern in einem Nachrichtendienst werden in ihren eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a56c3-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a56c3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a56c3-121">See also</span></span>



[<span data-ttu-id="a56c3-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a56c3-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a56c3-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a56c3-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

