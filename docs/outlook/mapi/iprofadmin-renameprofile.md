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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4453465c04d7a5a3de79f2ae34d13095863487cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569505"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="b2506-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="b2506-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="b2506-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2506-105">Weist einen neuen Namen zu einem Profil.</span><span class="sxs-lookup"><span data-stu-id="b2506-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b2506-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2506-106">Parameters</span></span>

 <span data-ttu-id="b2506-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="b2506-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="b2506-108">[in] Ein Zeiger auf den aktuellen Namen des Profils umbenennen.</span><span class="sxs-lookup"><span data-stu-id="b2506-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="b2506-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="b2506-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="b2506-110">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="b2506-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="b2506-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="b2506-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="b2506-112">[in] Ein Zeiger auf den neuen Namen des Profils umbenennen.</span><span class="sxs-lookup"><span data-stu-id="b2506-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="b2506-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b2506-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="b2506-114">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b2506-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="b2506-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2506-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b2506-116">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="b2506-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2506-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b2506-117">Return value</span></span>

<span data-ttu-id="b2506-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2506-118">S_OK</span></span> 
  
> <span data-ttu-id="b2506-119">Das Profil wurde erfolgreich umbenannt.</span><span class="sxs-lookup"><span data-stu-id="b2506-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="b2506-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="b2506-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="b2506-121">Das Profilkennwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="b2506-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="b2506-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b2506-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b2506-123">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b2506-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2506-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="b2506-124">Remarks</span></span>

<span data-ttu-id="b2506-125">Die **IProfAdmin::RenameProfile** -Methode weist einen neuen Namen zu einem Profil, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b2506-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="b2506-126">Wenn das Profil Umbenennen von einem Client wird **RenameProfile** aufgerufen wird, **RenameProfile** markiert das Profil und S_OK wird anstelle den Umbenennungsvorgang versucht, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2506-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="b2506-127">Wenn das Profil nicht mehr verwendet wird, weist ihm **RenameProfile** den neuen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="b2506-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="b2506-128">Die alten und neuen Namen des Profils können bis zu 64 Zeichen lang sein und können die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="b2506-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="b2506-129">Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="b2506-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="b2506-130">Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="b2506-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="b2506-131">Die _LpszPassword_ sollte immer NULL oder einen Zeiger auf eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b2506-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2506-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2506-132">See also</span></span>



[<span data-ttu-id="b2506-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2506-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

