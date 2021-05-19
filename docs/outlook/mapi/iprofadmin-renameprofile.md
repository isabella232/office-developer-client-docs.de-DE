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
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419520"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="04f8e-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="04f8e-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="04f8e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04f8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04f8e-105">Weist einem Profil einen neuen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="04f8e-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="04f8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04f8e-106">Parameters</span></span>

 <span data-ttu-id="04f8e-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="04f8e-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="04f8e-108">[in] Ein Zeiger auf den aktuellen Namen des Umbenennungsprofils.</span><span class="sxs-lookup"><span data-stu-id="04f8e-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="04f8e-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="04f8e-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="04f8e-110">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="04f8e-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="04f8e-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="04f8e-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="04f8e-112">[in] Ein Zeiger auf den neuen Namen des Umbenennungsprofils.</span><span class="sxs-lookup"><span data-stu-id="04f8e-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="04f8e-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="04f8e-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="04f8e-114">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="04f8e-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="04f8e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04f8e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="04f8e-116">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="04f8e-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04f8e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04f8e-117">Return value</span></span>

<span data-ttu-id="04f8e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="04f8e-118">S_OK</span></span> 
  
> <span data-ttu-id="04f8e-119">Das Profil wurde erfolgreich umbenannt.</span><span class="sxs-lookup"><span data-stu-id="04f8e-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="04f8e-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="04f8e-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="04f8e-121">Das Profilkennwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="04f8e-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="04f8e-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="04f8e-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="04f8e-123">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="04f8e-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="04f8e-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04f8e-124">Remarks</span></span>

<span data-ttu-id="04f8e-125">Die **IProfAdmin::RenameProfile-Methode** weist einem Profil einen neuen Namen zu, sofern er einen hat.</span><span class="sxs-lookup"><span data-stu-id="04f8e-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="04f8e-126">Wenn das umzubenennende Profil von einem Client verwendet wird, wenn **RenameProfile** aufgerufen wird, markiert **RenameProfile** das Profil und gibt S_OK zurück, anstatt den Umbenennungsvorgang zu versuchen, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04f8e-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="04f8e-127">Wenn das Profil nicht mehr verwendet wird, weist **RenameProfile** ihm den neuen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="04f8e-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="04f8e-128">Die alten und neuen Namen des Profils können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="04f8e-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="04f8e-129">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="04f8e-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="04f8e-130">Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="04f8e-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="04f8e-131">Das  _lpszPassword_ sollte immer NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein.</span><span class="sxs-lookup"><span data-stu-id="04f8e-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04f8e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04f8e-132">See also</span></span>



[<span data-ttu-id="04f8e-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04f8e-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

