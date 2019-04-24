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
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309968"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="b464f-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="b464f-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="b464f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b464f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b464f-105">Kopiert einen Nachrichtendienst in ein Profil.</span><span class="sxs-lookup"><span data-stu-id="b464f-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="b464f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b464f-106">Parameters</span></span>

 <span data-ttu-id="b464f-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="b464f-107">_lpUID_</span></span>
  
> <span data-ttu-id="b464f-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner des zu kopierende Nachrichtendiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="b464f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="b464f-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="b464f-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="b464f-110">in Dieser Parameter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="b464f-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="b464f-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="b464f-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="b464f-112">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profil Abschnitt des Nachrichtendiensts zum Kopieren verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b464f-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="b464f-113">Übergeben von NULL-Ergebnissen in der Standardprofil-Schnittstelle, [IProfSect](iprofsectimapiprop.md), wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="b464f-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="b464f-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="b464f-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="b464f-115">in Ein Zeiger auf die IID, die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das durch den _lpObjectDst_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b464f-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="b464f-116">Übergeben von NULL-Ergebnissen in der Sitzungs Schnittstelle, [IMAPISession](imapisessioniunknown.md), wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="b464f-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="b464f-117">Der _lpInterfaceDst_ -Parameter kann auch auf IID_IMsgServiceAdmin festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b464f-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="b464f-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="b464f-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="b464f-119">in Ein Zeiger auf einen Zeiger auf ein Sitzungs-oder Nachrichtendienst-Verwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b464f-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="b464f-120">Der Objekttyp sollte der Schnittstellenkennung entsprechen, die in _lpInterfaceDst_übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b464f-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="b464f-121">Gültige Objektzeiger sind LPMAPISESSION und LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="b464f-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="b464f-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b464f-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="b464f-123">in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b464f-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="b464f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b464f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="b464f-125">in Eine Bitmaske von Flags, die steuert, wie der Nachrichtendienst kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="b464f-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="b464f-126">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b464f-126">The following flags can be set:</span></span>
    
<span data-ttu-id="b464f-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="b464f-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="b464f-128">Fordert, dass der Nachrichtendienst immer ein Konfigurationseigenschaften Blatt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b464f-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b464f-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b464f-129">Return value</span></span>

<span data-ttu-id="b464f-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="b464f-130">S_OK</span></span> 
  
> <span data-ttu-id="b464f-131">Der Nachrichtendienst wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="b464f-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="b464f-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b464f-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b464f-133">Der Nachrichtendienst befindet sich bereits im Profil und lässt keine mehrere Instanzen von sich selbst zu.</span><span class="sxs-lookup"><span data-stu-id="b464f-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="b464f-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b464f-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b464f-135">Die **MAPIUID** , auf die durch _lpUID_ verwiesen wird, bezieht sich nicht auf einen vorhandenen Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="b464f-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b464f-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b464f-136">Remarks</span></span>

<span data-ttu-id="b464f-137">Die **IMsgServiceAdmin:: CopyMsgService** -Methode kopiert einen Nachrichtendienst in ein Profil, entweder das aktive Profil oder ein anderes Profil.</span><span class="sxs-lookup"><span data-stu-id="b464f-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="b464f-138">Das Profil, das den zu kopierenden Nachrichtendienst enthält, und das Ziel muss nicht dasselbe Profil aufweisen, aber möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="b464f-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="b464f-139">Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht für einen Kopiervorgang aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b464f-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="b464f-140">Der kopierte Nachrichtendienst hat die gleichen Konfigurationseinstellungen wie sein ursprüngliches.</span><span class="sxs-lookup"><span data-stu-id="b464f-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="b464f-141">Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b464f-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b464f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b464f-142">See also</span></span>



[<span data-ttu-id="b464f-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="b464f-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="b464f-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b464f-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b464f-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b464f-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

