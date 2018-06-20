---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792756"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="1e2d4-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="1e2d4-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="1e2d4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e2d4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e2d4-105">Weist einen neuen Namen zu einem Profil.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1e2d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e2d4-106">Parameters</span></span>

 <span data-ttu-id="1e2d4-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="1e2d4-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="1e2d4-108">[in] Ein Zeiger auf den aktuellen Namen des Profils umbenennen.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="1e2d4-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="1e2d4-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="1e2d4-110">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="1e2d4-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="1e2d4-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="1e2d4-112">[in] Ein Zeiger auf den neuen Namen des Profils umbenennen.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="1e2d4-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1e2d4-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="1e2d4-114">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="1e2d4-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e2d4-115">_ulFlags_</span></span>
  
> <span data-ttu-id="1e2d4-116">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e2d4-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1e2d4-117">Return value</span></span>

<span data-ttu-id="1e2d4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e2d4-118">S_OK</span></span> 
  
> <span data-ttu-id="1e2d4-119">Das Profil wurde erfolgreich umbenannt.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="1e2d4-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="1e2d4-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="1e2d4-121">Das Profilkennwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="1e2d4-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1e2d4-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1e2d4-123">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1e2d4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e2d4-124">Remarks</span></span>

<span data-ttu-id="1e2d4-125">Die **IProfAdmin::RenameProfile** -Methode weist einen neuen Namen zu einem Profil, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="1e2d4-126">Wenn das Profil Umbenennen von einem Client wird **RenameProfile** aufgerufen wird, **RenameProfile** markiert das Profil und S_OK wird anstelle den Umbenennungsvorgang versucht, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="1e2d4-127">Wenn das Profil nicht mehr verwendet wird, weist ihm **RenameProfile** den neuen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="1e2d4-128">Die alten und neuen Namen des Profils können bis zu 64 Zeichen lang sein und können die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="1e2d4-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="1e2d4-129">Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="1e2d4-130">Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="1e2d4-131">Die _LpszPassword_ sollte immer NULL oder einen Zeiger auf eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="1e2d4-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e2d4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e2d4-132">See also</span></span>



[<span data-ttu-id="1e2d4-133">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e2d4-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

