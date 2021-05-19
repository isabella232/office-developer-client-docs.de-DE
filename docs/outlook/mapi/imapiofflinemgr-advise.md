---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426919"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="93d26-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="93d26-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="93d26-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93d26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93d26-105">Registriert einen Client zum Empfangen von Rückrufen für ein Offlineobjekt.</span><span class="sxs-lookup"><span data-stu-id="93d26-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="93d26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93d26-106">Parameters</span></span>

 <span data-ttu-id="93d26-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="93d26-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="93d26-108">[in] Flags, die das Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="93d26-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="93d26-109">Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93d26-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="93d26-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="93d26-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="93d26-111">[in] Informationen zum Typ des Rückrufs, zum Empfang eines Rückrufs, einer Rückrufschnittstelle für den Anrufer und anderen Details.</span><span class="sxs-lookup"><span data-stu-id="93d26-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="93d26-112">Außerdem enthält es ein Clienttoken, das Outlook beim Senden nachfolgender Benachrichtigungsrückrufe an den Clientaufrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93d26-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="93d26-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="93d26-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="93d26-114">[out] Ein an den Clientaufrufer zurückgegebenes Ratschlagtoken zum anschließenden Abbrechen des Rückrufs für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="93d26-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93d26-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93d26-115">Return value</span></span>

<span data-ttu-id="93d26-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="93d26-116">S_OK</span></span>
  
> <span data-ttu-id="93d26-117">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="93d26-117">The call was successful.</span></span>
    
<span data-ttu-id="93d26-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="93d26-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="93d26-119">Ein ungültiger Parameter wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="93d26-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="93d26-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="93d26-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="93d26-121">Die in  *pAdviseInfo*  angegebene Rückrufschnittstelle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="93d26-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="93d26-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93d26-122">Remarks</span></span>

<span data-ttu-id="93d26-123">Beim Öffnen eines Offlineobjekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="93d26-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="93d26-124">Der Client kann mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** nach den Arten von Rückrufen suchen, die vom Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="93d26-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="93d26-125">Der Client kann den Typ und andere Details zu dem Rückruf bestimmen, den er möchte, und dann **IMAPIOfflineMgr::Advise** aufrufen, sich zu registrieren, um solche Rückrufe für das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93d26-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93d26-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93d26-126">See also</span></span>



[<span data-ttu-id="93d26-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="93d26-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="93d26-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="93d26-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="93d26-129">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="93d26-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="93d26-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="93d26-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

