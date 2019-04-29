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
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="b2c3d-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="b2c3d-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="b2c3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2c3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2c3d-105">Registriert einen Client für den Empfang von Rückrufen für ein Offlineobjekt.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="b2c3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c3d-106">Parameters</span></span>

 <span data-ttu-id="b2c3d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2c3d-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="b2c3d-108">in Kennzeichen, die das Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="b2c3d-109">Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="b2c3d-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="b2c3d-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="b2c3d-111">in Informationen zum Rückruftyp, zum Empfang eines Rückrufs, eine Rückrufschnittstelle für den Anrufer und weitere Details.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="b2c3d-112">Außerdem enthält es ein Clienttoken, das Outlook beim Senden von nachfolgenden Benachrichtigungs Rückrufen an den Client Aufrufer verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="b2c3d-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="b2c3d-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="b2c3d-114">Out Ein Advise-Token, das an den Aufrufer des Clients zurückgegeben wird, um den Rückruf für das Objekt abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2c3d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2c3d-115">Return value</span></span>

<span data-ttu-id="b2c3d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2c3d-116">S_OK</span></span>
  
> <span data-ttu-id="b2c3d-117">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-117">The call was successful.</span></span>
    
<span data-ttu-id="b2c3d-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b2c3d-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="b2c3d-119">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="b2c3d-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="b2c3d-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="b2c3d-121">Die in *pAdviseInfo* angegebene Rückrufschnittstelle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2c3d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2c3d-122">Remarks</span></span>

<span data-ttu-id="b2c3d-123">Beim Öffnen eines Offline Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** Ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="b2c3d-124">Der Client kann die vom Objekt unterstützten Rückruf Typen mithilfe von **[IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="b2c3d-125">Der Client kann den Typ und weitere Details zu dem gewünschten Rückruf ermitteln und dann **IMAPIOfflineMgr:: Advise** aufrufen, um sich für das empfangen solcher Rückrufe über das Objekt zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b2c3d-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2c3d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2c3d-126">See also</span></span>



[<span data-ttu-id="b2c3d-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b2c3d-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="b2c3d-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b2c3d-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="b2c3d-129">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b2c3d-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b2c3d-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b2c3d-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

