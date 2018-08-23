---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587705"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="ac430-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac430-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="ac430-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac430-105">Aktiviert oder deaktiviert eine Client-Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ac430-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ac430-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac430-106">Parameters</span></span>

 <span data-ttu-id="ac430-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ac430-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ac430-108">[in] Ein Zeiger auf den Namen des Profils, das werden die Standardeinstellung, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="ac430-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="ac430-109">_LpszProfileName_ bedeutet von NULL, dass **SetDefaultProfile** vorhandenen Standardprofils entfernen sollte den Client ohne Standardwert verlassen.</span><span class="sxs-lookup"><span data-stu-id="ac430-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="ac430-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac430-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ac430-111">[in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolge steuert auf _LpszProfileName_zeigt.</span><span class="sxs-lookup"><span data-stu-id="ac430-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="ac430-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ac430-112">The following flag can be set:</span></span>
    
<span data-ttu-id="ac430-113">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac430-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ac430-114">Der Name der Benutzerprofildienst wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ac430-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="ac430-115">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name der Benutzerprofildienst im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ac430-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac430-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ac430-116">Return value</span></span>

<span data-ttu-id="ac430-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac430-117">S_OK</span></span> 
  
> <span data-ttu-id="ac430-118">Ein Standardprofil wurde erfolgreich hergestellt oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac430-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="ac430-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac430-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ac430-120">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac430-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac430-121">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ac430-121">Remarks</span></span>

<span data-ttu-id="ac430-122">Die **IProfAdmin::SetDefaultProfile** -Methode stellt ein bestimmtes Profil als Standardprofil für den Client her, oder löscht den aktuellen Standardprofils.</span><span class="sxs-lookup"><span data-stu-id="ac430-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="ac430-123">Das Standardprofil ist das Profil, das automatisch verwendet wird, wenn der Client eine MAPI-Sitzung beginnt.</span><span class="sxs-lookup"><span data-stu-id="ac430-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="ac430-124">**SetDefaultProfile** wird auch neues Standardprofil **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))-Eigenschaft auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac430-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac430-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ac430-125">Notes to callers</span></span>

<span data-ttu-id="ac430-126">Um eine Sitzung mit dem Standardprofil starten möchten, übergeben Sie die Kennzeichen MAPI_USE_DEFAULT an die Funktion [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="ac430-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac430-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac430-127">See also</span></span>



[<span data-ttu-id="ac430-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="ac430-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="ac430-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ac430-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="ac430-130">PidTagDefaultProfile (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ac430-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="ac430-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac430-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

