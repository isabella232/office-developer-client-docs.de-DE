---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792614"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="03ddc-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="03ddc-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="03ddc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03ddc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03ddc-105">Kopiert eine Message Service in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="03ddc-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="03ddc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ddc-106">Parameters</span></span>

 <span data-ttu-id="03ddc-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="03ddc-107">_lpUID_</span></span>
  
> <span data-ttu-id="03ddc-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner des Diensts zum Kopieren von Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="03ddc-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="03ddc-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="03ddc-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="03ddc-110">[in] Dieser Parameter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="03ddc-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="03ddc-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="03ddc-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="03ddc-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt des Diensts zum Kopieren von Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03ddc-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="03ddc-113">Bei Übergabe von NULL führt die Standardprofil Abschnitt-Schnittstelle, [IProfSect](iprofsectimapiprop.md), verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03ddc-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="03ddc-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="03ddc-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="03ddc-115">[in] Ein Zeiger auf die IID, die die Schnittstelle verwendet werden, um Zugriff auf das Objekt, durch den Parameter _LpObjectDst_ auf darstellt.</span><span class="sxs-lookup"><span data-stu-id="03ddc-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="03ddc-116">Bei Übergabe von NULL führt die Sitzungsschnittstelle, [IMAPISession](imapisessioniunknown.md), verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03ddc-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="03ddc-117">Der Parameter _LpInterfaceDst_ kann auch auf IID_IMsgServiceAdmin festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="03ddc-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="03ddc-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="03ddc-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="03ddc-119">[in] Ein Zeiger auf einen Zeiger auf eine Sitzung oder einer Nachricht Service Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03ddc-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="03ddc-120">Der Identifier übergebenen _LpInterfaceDst_sollte der Typ des Objekts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="03ddc-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="03ddc-121">Gültige Objektzeigern sind LPMAPISESSION und LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="03ddc-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="03ddc-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="03ddc-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="03ddc-123">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="03ddc-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="03ddc-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03ddc-124">_ulFlags_</span></span>
  
> <span data-ttu-id="03ddc-125">[in] Eine Bitmaske aus Flags, die steuert, wie der Nachrichtendienst kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="03ddc-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="03ddc-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="03ddc-126">The following flags can be set:</span></span>
    
<span data-ttu-id="03ddc-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="03ddc-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="03ddc-128">Fordert, dass die Messagingdiensts immer eine Konfiguration Eigenschaftenfenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="03ddc-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03ddc-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03ddc-129">Return value</span></span>

<span data-ttu-id="03ddc-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="03ddc-130">S_OK</span></span> 
  
> <span data-ttu-id="03ddc-131">Der Nachrichtendienst wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="03ddc-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="03ddc-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="03ddc-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="03ddc-133">Message-Dienst ist bereits im Profil und lässt nicht mehrere Instanzen von sich selbst.</span><span class="sxs-lookup"><span data-stu-id="03ddc-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="03ddc-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="03ddc-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="03ddc-135">Die **MAPIUID** auf das _LpUID_ bezieht sich nicht auf einem vorhandenen Meldung-Dienst.</span><span class="sxs-lookup"><span data-stu-id="03ddc-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="03ddc-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03ddc-136">Remarks</span></span>

<span data-ttu-id="03ddc-137">Die **IMsgServiceAdmin::CopyMsgService** -Methode kopiert eine Message Service in einem Profil, das aktive Profil oder ein anderes Profil.</span><span class="sxs-lookup"><span data-stu-id="03ddc-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="03ddc-138">Das Profil, das den Dienst zu kopierenden enthält, und das Ziel müssen nicht das gleiche Profil werden, aber sie werden können.</span><span class="sxs-lookup"><span data-stu-id="03ddc-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="03ddc-139">Die Messagingdiensts Eintrag Point-Funktion ist nicht für einen Kopiervorgang aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="03ddc-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="03ddc-140">Die kopierten Messagingdiensts hat die gleiche Konfigurationseinstellungen als den ursprünglichen.</span><span class="sxs-lookup"><span data-stu-id="03ddc-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="03ddc-141">Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03ddc-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03ddc-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ddc-142">See also</span></span>



[<span data-ttu-id="03ddc-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="03ddc-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="03ddc-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="03ddc-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="03ddc-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03ddc-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

