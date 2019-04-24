---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309569"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="0c31b-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="0c31b-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="0c31b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c31b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c31b-105">Kopiert ein Profil.</span><span class="sxs-lookup"><span data-stu-id="0c31b-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0c31b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c31b-106">Parameters</span></span>

 <span data-ttu-id="0c31b-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="0c31b-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="0c31b-108">in Ein Zeiger auf den Namen des zu kopierende Profils.</span><span class="sxs-lookup"><span data-stu-id="0c31b-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="0c31b-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="0c31b-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="0c31b-110">in Ein Zeiger auf das Kennwort des zu kopierende Profils.</span><span class="sxs-lookup"><span data-stu-id="0c31b-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="0c31b-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="0c31b-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="0c31b-112">in Ein Zeiger auf den neuen Namen des kopierten Profils.</span><span class="sxs-lookup"><span data-stu-id="0c31b-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="0c31b-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0c31b-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="0c31b-114">in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="0c31b-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="0c31b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c31b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0c31b-116">in Eine Bitmaske von Flags, die das Kopieren des Profils steuert.</span><span class="sxs-lookup"><span data-stu-id="0c31b-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="0c31b-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0c31b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="0c31b-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0c31b-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="0c31b-119">Zeigt ein Dialogfeld an, in dem der Benutzer das richtige Kennwort des zu kopierenden Profils auffordert.</span><span class="sxs-lookup"><span data-stu-id="0c31b-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="0c31b-120">Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c31b-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c31b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c31b-121">Return value</span></span>

<span data-ttu-id="0c31b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c31b-122">S_OK</span></span> 
  
> <span data-ttu-id="0c31b-123">Das Profil wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="0c31b-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="0c31b-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="0c31b-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="0c31b-125">Der neue Profilname ist derselbe wie der eines vorhandenen Profils.</span><span class="sxs-lookup"><span data-stu-id="0c31b-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="0c31b-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="0c31b-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="0c31b-127">Das Kennwort für das zu kopierende Profil ist falsch, und dem Benutzer kann kein Dialogfeld angezeigt werden, das das richtige Kennwort anfordert, da MAPI_DIALOG nicht im _ulFlags_ -Parameter festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c31b-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="0c31b-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0c31b-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0c31b-129">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0c31b-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="0c31b-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0c31b-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0c31b-131">Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="0c31b-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c31b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c31b-132">Remarks</span></span>

<span data-ttu-id="0c31b-133">Die **IProfAdmin:: CopyProfile** -Methode erstellt eine Kopie des Profils, auf die von _lpszOldProfileName_verwiesen wird, und gibt ihr den Namen, auf den _lpszNewProfileName_verweist.</span><span class="sxs-lookup"><span data-stu-id="0c31b-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="0c31b-134">Beim Kopieren eines Profils wird die Kopie mit dem gleichen Kennwort wie das Original kopiert.</span><span class="sxs-lookup"><span data-stu-id="0c31b-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="0c31b-135">Der Name des ursprünglichen Profils, sein Kennwort und die Kopie können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="0c31b-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="0c31b-136">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und der Unterstrich.</span><span class="sxs-lookup"><span data-stu-id="0c31b-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="0c31b-137">Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="0c31b-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="0c31b-138">Profil Kennwörter werden auf allen Betriebssystemen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c31b-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="0c31b-139">Auf Betriebssystemen, die Profil Kennwörter nicht unterstützen, kann _LPSZOLDPASSWORD_ NULL oder ein Zeiger auf eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="0c31b-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="0c31b-140">Wenn _lpszOldPassword_ auf NULL festgelegt ist, erfordert das zu kopierende Profil ein Kennwort, und das MAPI_DIALOG-Flag wird festgelegt; ein Dialogfeld, in dem der Benutzer aufgefordert wird, das Kennwort anzugeben, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c31b-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="0c31b-141">Wenn ein Kennwort erforderlich ist, aber _lpszOldPassword_ auf NULL festgelegt ist und das MAPI_DIALOG-Flag nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED zurück.</span><span class="sxs-lookup"><span data-stu-id="0c31b-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c31b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c31b-142">See also</span></span>



[<span data-ttu-id="0c31b-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c31b-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

