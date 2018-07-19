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
ms.openlocfilehash: 53fa6bd49190bb88daeb0438dc0112e34322383e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792248"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="b2adf-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="b2adf-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="b2adf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2adf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2adf-105">Registriert einen Client für Rückrufe für eine offline-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2adf-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="b2adf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2adf-106">Parameters</span></span>

 <span data-ttu-id="b2adf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2adf-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="b2adf-108">[in] Kennzeichen, die Verhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b2adf-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="b2adf-109">Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2adf-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="b2adf-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="b2adf-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="b2adf-111">[in] Informationen zu den Typ des Rückrufs, wann ein Rückruf, eine Callback-Schnittstelle für den Anrufer sowie andere Details zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2adf-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="b2adf-112">Sie enthält außerdem eine Clienttoken, die Outlook verwendet, nachfolgende Benachrichtigung Rückrufe an den Client Anrufer senden.</span><span class="sxs-lookup"><span data-stu-id="b2adf-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="b2adf-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="b2adf-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="b2adf-114">[out] Ein Advise-Token an den Clientaufrufer für anschließend stornieren Rückruf für das Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2adf-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2adf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2adf-115">Return value</span></span>

<span data-ttu-id="b2adf-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2adf-116">S_OK</span></span>
  
> <span data-ttu-id="b2adf-117">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b2adf-117">The call was successful.</span></span>
    
<span data-ttu-id="b2adf-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b2adf-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="b2adf-119">Ein ungültiger Parameter es wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2adf-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="b2adf-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="b2adf-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="b2adf-121">Die Callback-Schnittstelle in *pAdviseInfo* angegebenen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b2adf-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2adf-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2adf-122">Remarks</span></span>

<span data-ttu-id="b2adf-123">Beim Öffnen einer offline-Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)**, erhält ein Client eine offline-Objekt, das **IMAPIOfflineMgr**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2adf-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="b2adf-124">Der Client kann für die Arten von mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** durch das Objekt unterstützt Rückrufe überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b2adf-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="b2adf-125">Der Client kann bestimmen, den Typ sowie andere Details zu den Rückruf es möchte, und rufen Sie dann **IMAPIOfflineMgr::Advise** registrieren, um eine solche Rückrufe zum Objekt empfangen.</span><span class="sxs-lookup"><span data-stu-id="b2adf-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2adf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2adf-126">See also</span></span>



[<span data-ttu-id="b2adf-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b2adf-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="b2adf-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b2adf-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="b2adf-129">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b2adf-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b2adf-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b2adf-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

