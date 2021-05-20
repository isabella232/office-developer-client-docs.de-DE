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
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439625"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="e991d-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e991d-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="e991d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e991d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e991d-105">Legt das Standardprofil eines Clients fest oder deaktiviert es.</span><span class="sxs-lookup"><span data-stu-id="e991d-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e991d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e991d-106">Parameters</span></span>

 <span data-ttu-id="e991d-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="e991d-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="e991d-108">[in] Ein Zeiger auf den Namen des Profils, das zur Standardeinstellung wird, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="e991d-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="e991d-109">Das  _Festlegen von lpszProfileName_ auf NULL gibt an, dass **SetDefaultProfile** das vorhandene Standardprofil entfernen soll, ohne dass der Client einen Standardwert hat.</span><span class="sxs-lookup"><span data-stu-id="e991d-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="e991d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e991d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e991d-111">[in] Eine Bitmaske mit Flags, die den Typ der Zeichenfolge steuert, auf die _von lpszProfileName verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="e991d-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="e991d-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e991d-112">The following flag can be set:</span></span>
    
<span data-ttu-id="e991d-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e991d-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e991d-114">Der Profilname ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e991d-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="e991d-115">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Profilname im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e991d-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e991d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e991d-116">Return value</span></span>

<span data-ttu-id="e991d-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="e991d-117">S_OK</span></span> 
  
> <span data-ttu-id="e991d-118">Ein Standardprofil wurde erfolgreich eingerichtet oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="e991d-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="e991d-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e991d-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e991d-120">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e991d-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e991d-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e991d-121">Remarks</span></span>

<span data-ttu-id="e991d-122">Die **IProfAdmin::SetDefaultProfile-Methode** richtet entweder ein bestimmtes Profil als Standardprofil des Clients ein oder deaktiviert das aktuelle Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e991d-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="e991d-123">Das Standardprofil ist das Profil, das automatisch verwendet wird, wenn der Client eine MAPI-Sitzung beginnt.</span><span class="sxs-lookup"><span data-stu-id="e991d-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="e991d-124">**SetDefaultProfile** legt außerdem die Eigenschaft **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) des neuen Standardprofils auf TRUE fest.</span><span class="sxs-lookup"><span data-stu-id="e991d-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e991d-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e991d-125">Notes to callers</span></span>

<span data-ttu-id="e991d-126">Um eine Sitzung mit dem Standardprofil zu starten, übergeben Sie das MAPI_USE_DEFAULT an die [MAPILogonEx-Funktion.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="e991d-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e991d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e991d-127">See also</span></span>



[<span data-ttu-id="e991d-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="e991d-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="e991d-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="e991d-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="e991d-130">PidTagDefaultProfile (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e991d-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="e991d-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e991d-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

