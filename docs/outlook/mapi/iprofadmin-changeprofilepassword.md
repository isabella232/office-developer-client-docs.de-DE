---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 41066d4418760a676fbc02241bfc12d83275da9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572998"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="52ffb-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="52ffb-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="52ffb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52ffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52ffb-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="52ffb-105">Deprecated.</span></span> <span data-ttu-id="52ffb-106">Ändert das Kennwort für ein Profil.</span><span class="sxs-lookup"><span data-stu-id="52ffb-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="52ffb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="52ffb-107">Parameters</span></span>

 <span data-ttu-id="52ffb-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="52ffb-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="52ffb-109">[in] Ein Zeiger auf den Namen des Profils, das Kennwort zu ändernden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="52ffb-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="52ffb-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="52ffb-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="52ffb-111">[in] Ein Zeiger auf das aktuelle Kennwort.</span><span class="sxs-lookup"><span data-stu-id="52ffb-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="52ffb-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="52ffb-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="52ffb-113">[in] Ein Zeiger auf das neue Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="52ffb-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="52ffb-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52ffb-114">_ulFlags_</span></span>
  
> <span data-ttu-id="52ffb-115">[in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="52ffb-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="52ffb-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="52ffb-116">The following flag can be set:</span></span>
    
<span data-ttu-id="52ffb-117">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="52ffb-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="52ffb-118">Der Name der Benutzerprofildienst und Kennwörter werden im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="52ffb-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="52ffb-119">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="52ffb-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52ffb-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="52ffb-120">Return value</span></span>

<span data-ttu-id="52ffb-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="52ffb-121">S_OK</span></span> 
  
> <span data-ttu-id="52ffb-122">Wenn diese Methode aufgerufen wird, wird S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52ffb-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="52ffb-123">Es wird jedoch keine Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="52ffb-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52ffb-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="52ffb-124">Remarks</span></span>

<span data-ttu-id="52ffb-125">Verwenden Sie diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="52ffb-125">Do not use this method.</span></span> <span data-ttu-id="52ffb-126">MAPI unterstützt keine Kennwörter für Profile.</span><span class="sxs-lookup"><span data-stu-id="52ffb-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52ffb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52ffb-127">See also</span></span>



[<span data-ttu-id="52ffb-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52ffb-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

