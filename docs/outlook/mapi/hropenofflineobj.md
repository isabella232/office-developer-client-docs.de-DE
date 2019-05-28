---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347747"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="b49bb-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b49bb-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="b49bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b49bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b49bb-105">Öffnet ein Offlineobjekt basierend auf einem bestimmten Profil.</span><span class="sxs-lookup"><span data-stu-id="b49bb-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b49bb-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b49bb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b49bb-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="b49bb-107">Exported by:</span></span>  <br/> |<span data-ttu-id="b49bb-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="b49bb-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="b49bb-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b49bb-109">Called by:</span></span>  <br/> |<span data-ttu-id="b49bb-110">Client</span><span class="sxs-lookup"><span data-stu-id="b49bb-110">Client</span></span>  <br/> |
|<span data-ttu-id="b49bb-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b49bb-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b49bb-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="b49bb-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="b49bb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b49bb-113">Parameters</span></span>

 <span data-ttu-id="b49bb-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="b49bb-114">_ulReserved_</span></span>
  
> <span data-ttu-id="b49bb-115">in Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b49bb-115">[in] This parameter is not used.</span></span> <span data-ttu-id="b49bb-116">Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="b49bb-116">It must be 0.</span></span>
    
 <span data-ttu-id="b49bb-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="b49bb-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="b49bb-118">in Der Name des Profils, für das das Offlineobjekt gilt.</span><span class="sxs-lookup"><span data-stu-id="b49bb-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="b49bb-119">Es muss in Unicode ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="b49bb-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="b49bb-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="b49bb-120">_pGUID_</span></span>
  
> <span data-ttu-id="b49bb-121">in Zeiger auf eine GUID, die verwendet werden kann, um dieses Objekt von anderen Offlineobjekten eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b49bb-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="b49bb-122">Es muss **GUID_GlobalState**sein.</span><span class="sxs-lookup"><span data-stu-id="b49bb-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="b49bb-123">_beibehalten_</span><span class="sxs-lookup"><span data-stu-id="b49bb-123">_pReserved_</span></span>
  
> <span data-ttu-id="b49bb-124">in Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b49bb-124">[in] This parameter is not used.</span></span> <span data-ttu-id="b49bb-125">Es muss **null**sein.</span><span class="sxs-lookup"><span data-stu-id="b49bb-125">It must be **null**.</span></span>
    
 <span data-ttu-id="b49bb-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="b49bb-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="b49bb-127">Timeout Ein Zeiger auf das angeforderte Offlineobjekt.</span><span class="sxs-lookup"><span data-stu-id="b49bb-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="b49bb-128">Der Aufrufer kann mit diesem Zeiger auf die [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) -Schnittstelle zugreifen, um die Rückrufe zu finden, die dieses Objekt unterstützt, und um Rückrufe dafür einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b49bb-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b49bb-129">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b49bb-129">Return values</span></span>

<span data-ttu-id="b49bb-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="b49bb-130">S_OK</span></span> 
  
- <span data-ttu-id="b49bb-131">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b49bb-131">The function call is successful.</span></span>
    
<span data-ttu-id="b49bb-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b49bb-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="b49bb-133">Der Funktionsaufruf ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="b49bb-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b49bb-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b49bb-134">Remarks</span></span>

<span data-ttu-id="b49bb-135">Dies ist der erste Anruf, den ein Client vornimmt, wenn der Client über etwaige Verbindungsstatusänderungen für ein bestimmtes Profil benachrichtigt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="b49bb-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="b49bb-136">Beim Aufruf von **HrOpenOfflineObj**ruft der Client ein Offlineobjekt ab, das **IMAPIOfflineMgr**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b49bb-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="b49bb-137">Der Client kann nach den vom Objekt unterstützten Arten von Rückrufen suchen (mithilfe von [IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)) und dann Rückrufe für ihn einrichten (mithilfe von [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="b49bb-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="b49bb-138">Wenn Sie [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie **HrOpenOfflineObj @ 20** als Prozedurnamen an.</span><span class="sxs-lookup"><span data-stu-id="b49bb-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="b49bb-139">**HrOpenOfflineObj** funktioniert nur für Clients, bei denen es sich um MAPI-Anbieter, COM-Add-Ins und Exchange-Client Erweiterungen handelt, die innerhalb des Outlook-Prozesses ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b49bb-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="b49bb-140">Andernfalls gibt **HrOpenOfflineObj** **MAPI_E_NOT_FOUND**zurück.</span><span class="sxs-lookup"><span data-stu-id="b49bb-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b49bb-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b49bb-141">See also</span></span>



[<span data-ttu-id="b49bb-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b49bb-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="b49bb-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="b49bb-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="b49bb-144">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="b49bb-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="b49bb-145">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b49bb-145">MAPI Constants</span></span>](mapi-constants.md)

