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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579522"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="ab1b7-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ab1b7-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="ab1b7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab1b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab1b7-105">Bricht Rückrufe für eine offline-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="ab1b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab1b7-106">Parameters</span></span>

 <span data-ttu-id="ab1b7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab1b7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ab1b7-108">[in] Flags für das Abbrechen Rückruf.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="ab1b7-109">Nur der Wert MAPIOFFLINE_UNADVISE_DEFAULT wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="ab1b7-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="ab1b7-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="ab1b7-111">[in] Ein Advise-Token, das die Rückruf Registrierung identifiziert, die abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab1b7-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ab1b7-112">Return value</span></span>

<span data-ttu-id="ab1b7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab1b7-113">S_OK</span></span>
  
> <span data-ttu-id="ab1b7-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-114">The call was successful.</span></span> <span data-ttu-id="ab1b7-115">Dieser Aufruf muss S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab1b7-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ab1b7-116">Remarks</span></span>

<span data-ttu-id="ab1b7-117">Entfernt die Registrierung des Rückrufs, die mit *UlAdviseToken* zurückgegeben, die von einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="ab1b7-118">Bewirkt, dass das **IMAPIOfflineMgr** -Objekt, das den Verweis auf das zugeordnete *UlAdviseToken* **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** -Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="ab1b7-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab1b7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab1b7-119">See also</span></span>



[<span data-ttu-id="ab1b7-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="ab1b7-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="ab1b7-121">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ab1b7-121">MAPI Constants</span></span>](mapi-constants.md)

