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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792614"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="97a1a-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="97a1a-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="97a1a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97a1a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97a1a-105">Kopiert eine Message Service in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="97a1a-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="97a1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a1a-106">Parameters</span></span>

 <span data-ttu-id="97a1a-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="97a1a-107">_lpUID_</span></span>
  
> <span data-ttu-id="97a1a-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner des Diensts zum Kopieren von Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="97a1a-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="97a1a-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="97a1a-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="97a1a-110">[in] Dieser Parameter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="97a1a-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="97a1a-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="97a1a-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="97a1a-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt des Diensts zum Kopieren von Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97a1a-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="97a1a-113">Bei Übergabe von NULL führt die Standardprofil Abschnitt-Schnittstelle, [IProfSect](iprofsectimapiprop.md), verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97a1a-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="97a1a-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="97a1a-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="97a1a-115">[in] Ein Zeiger auf die IID, die die Schnittstelle verwendet werden, um Zugriff auf das Objekt, durch den Parameter _LpObjectDst_ auf darstellt.</span><span class="sxs-lookup"><span data-stu-id="97a1a-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="97a1a-116">Bei Übergabe von NULL führt die Sitzungsschnittstelle, [IMAPISession](imapisessioniunknown.md), verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97a1a-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="97a1a-117">Der Parameter _LpInterfaceDst_ kann auch auf IID_IMsgServiceAdmin festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="97a1a-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="97a1a-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="97a1a-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="97a1a-119">[in] Ein Zeiger auf einen Zeiger auf eine Sitzung oder einer Nachricht Service Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="97a1a-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="97a1a-120">Der Identifier übergebenen _LpInterfaceDst_sollte der Typ des Objekts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="97a1a-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="97a1a-121">Gültige Objektzeigern sind LPMAPISESSION und LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="97a1a-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="97a1a-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="97a1a-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="97a1a-123">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="97a1a-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="97a1a-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97a1a-124">_ulFlags_</span></span>
  
> <span data-ttu-id="97a1a-125">[in] Eine Bitmaske aus Flags, die steuert, wie der Nachrichtendienst kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="97a1a-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="97a1a-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="97a1a-126">The following flags can be set:</span></span>
    
<span data-ttu-id="97a1a-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="97a1a-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="97a1a-128">Fordert, dass die Messagingdiensts immer eine Konfiguration Eigenschaftenfenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="97a1a-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="97a1a-129">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="97a1a-129">Return value</span></span>

<span data-ttu-id="97a1a-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="97a1a-130">S_OK</span></span> 
  
> <span data-ttu-id="97a1a-131">Der Nachrichtendienst wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="97a1a-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="97a1a-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="97a1a-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="97a1a-133">Message-Dienst ist bereits im Profil und lässt nicht mehrere Instanzen von sich selbst.</span><span class="sxs-lookup"><span data-stu-id="97a1a-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="97a1a-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="97a1a-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="97a1a-135">Die **MAPIUID** auf das _LpUID_ bezieht sich nicht auf einem vorhandenen Meldung-Dienst.</span><span class="sxs-lookup"><span data-stu-id="97a1a-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="97a1a-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97a1a-136">Remarks</span></span>

<span data-ttu-id="97a1a-137">Die **IMsgServiceAdmin::CopyMsgService** -Methode kopiert eine Message Service in einem Profil, das aktive Profil oder ein anderes Profil.</span><span class="sxs-lookup"><span data-stu-id="97a1a-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="97a1a-138">Das Profil, das den Dienst zu kopierenden enthält, und das Ziel müssen nicht das gleiche Profil werden, aber sie werden können.</span><span class="sxs-lookup"><span data-stu-id="97a1a-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="97a1a-139">Die Messagingdiensts Eintrag Point-Funktion ist nicht für einen Kopiervorgang aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="97a1a-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="97a1a-140">Die kopierten Messagingdiensts hat die gleiche Konfigurationseinstellungen als den ursprünglichen.</span><span class="sxs-lookup"><span data-stu-id="97a1a-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="97a1a-141">Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="97a1a-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97a1a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a1a-142">See also</span></span>



[<span data-ttu-id="97a1a-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="97a1a-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="97a1a-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="97a1a-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="97a1a-145">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="97a1a-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

