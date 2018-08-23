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
ms.openlocfilehash: cc71974d841005785932cc9017d44c3c0614687d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563387"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="95d03-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="95d03-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="95d03-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95d03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95d03-105">Öffnet eine offline-Objekt basierend auf einem bestimmten Profil.</span><span class="sxs-lookup"><span data-stu-id="95d03-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="95d03-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="95d03-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95d03-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="95d03-107">Exported by:</span></span>  <br/> |<span data-ttu-id="95d03-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="95d03-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="95d03-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="95d03-109">Called by:</span></span>  <br/> |<span data-ttu-id="95d03-110">Client</span><span class="sxs-lookup"><span data-stu-id="95d03-110">Client</span></span>  <br/> |
|<span data-ttu-id="95d03-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="95d03-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="95d03-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="95d03-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="95d03-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="95d03-113">Parameters</span></span>

 <span data-ttu-id="95d03-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="95d03-114">_ulReserved_</span></span>
  
> <span data-ttu-id="95d03-115">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="95d03-115">[in] This parameter is not used.</span></span> <span data-ttu-id="95d03-116">Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="95d03-116">It must be 0.</span></span>
    
 <span data-ttu-id="95d03-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="95d03-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="95d03-118">[in] Der Name des Profils, das für das offline-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="95d03-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="95d03-119">Es muss in Unicode ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="95d03-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="95d03-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="95d03-120">_pGUID_</span></span>
  
> <span data-ttu-id="95d03-121">[in] Zeiger auf eine GUID, die verwendet werden kann, um dieses Objekt von anderen Objekten offline eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="95d03-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="95d03-122">Es muss **GUID_GlobalState**sein.</span><span class="sxs-lookup"><span data-stu-id="95d03-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="95d03-123">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="95d03-123">_pReserved_</span></span>
  
> <span data-ttu-id="95d03-124">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="95d03-124">[in] This parameter is not used.</span></span> <span data-ttu-id="95d03-125">Es muss **null**sein.</span><span class="sxs-lookup"><span data-stu-id="95d03-125">It must be **null**.</span></span>
    
 <span data-ttu-id="95d03-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="95d03-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="95d03-127">[out] Ein Zeiger auf das angeforderte offline-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95d03-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="95d03-128">Der Aufrufer kann diesen Zeiger verwenden, für den Zugriff auf die [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) Schnittstelle, die Rückrufe zu erhalten, die dieses Objekt unterstützt und Rückrufe dafür einzurichten.</span><span class="sxs-lookup"><span data-stu-id="95d03-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="95d03-129">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="95d03-129">Return values</span></span>

<span data-ttu-id="95d03-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="95d03-130">S_OK</span></span> 
  
- <span data-ttu-id="95d03-131">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="95d03-131">The function call is successful.</span></span>
    
<span data-ttu-id="95d03-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="95d03-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="95d03-133">Fehler beim Aufruf der Funktion.</span><span class="sxs-lookup"><span data-stu-id="95d03-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95d03-134">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="95d03-134">Remarks</span></span>

<span data-ttu-id="95d03-135">Dies ist der erste Aufruf, den ein Client sendet, wenn der Client über Änderungen Zustand Verbindung für ein bestimmtes Profil benachrichtigt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="95d03-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="95d03-136">Beim Aufrufen **HrOpenOfflineObj**, erhält der Client eine offline-Objekt, das **IMAPIOfflineMgr**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95d03-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="95d03-137">Der Client kann prüfen, ob die Arten von Rückrufe (mithilfe von [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) durch das Objekt unterstützt, und klicken Sie dann eingerichtet Rückrufe (mithilfe von [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="95d03-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="95d03-138">Wenn [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) für die Adresse des dieser Funktion in msmapi32.dll suchen, geben Sie **HrOpenOfflineObj@20** als den Namen der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="95d03-138">When using [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="95d03-139">**HrOpenOfflineObj** funktioniert nur für Clients, die MAPI-Anbieter, COM-Add-Ins und Exchange-Clienterweiterungen innerhalb des Outlook ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95d03-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="95d03-140">Andernfalls **HrOpenOfflineObj** **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="95d03-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95d03-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95d03-141">See also</span></span>



[<span data-ttu-id="95d03-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95d03-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="95d03-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="95d03-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="95d03-144">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="95d03-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="95d03-145">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="95d03-145">MAPI Constants</span></span>](mapi-constants.md)

