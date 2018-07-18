---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792254"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="a4021-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a4021-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="a4021-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4021-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4021-105">Bricht Rückrufe für eine offline-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="a4021-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="a4021-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4021-106">Parameters</span></span>

 <span data-ttu-id="a4021-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4021-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a4021-108">[in] Flags für das Abbrechen Rückruf.</span><span class="sxs-lookup"><span data-stu-id="a4021-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="a4021-109">Nur der Wert MAPIOFFLINE_UNADVISE_DEFAULT wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4021-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="a4021-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="a4021-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="a4021-111">[in] Ein Advise-Token, das die Rückruf Registrierung identifiziert, die abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4021-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a4021-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a4021-112">Return value</span></span>

<span data-ttu-id="a4021-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4021-113">S_OK</span></span>
  
> <span data-ttu-id="a4021-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a4021-114">The call was successful.</span></span> <span data-ttu-id="a4021-115">Dieser Aufruf muss S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a4021-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4021-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4021-116">Remarks</span></span>

<span data-ttu-id="a4021-117">Entfernt die Registrierung des Rückrufs, die mit *UlAdviseToken* zurückgegeben, die von einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a4021-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="a4021-118">Bewirkt, dass das **IMAPIOfflineMgr** -Objekt, das den Verweis auf das zugeordnete *UlAdviseToken* **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** -Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="a4021-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4021-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4021-119">See also</span></span>



[<span data-ttu-id="a4021-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="a4021-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="a4021-121">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a4021-121">MAPI Constants</span></span>](mapi-constants.md)

