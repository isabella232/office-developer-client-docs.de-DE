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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792761"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="081f9-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="081f9-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="081f9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="081f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="081f9-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="081f9-105">Deprecated.</span></span> <span data-ttu-id="081f9-106">Ändert das Kennwort für ein Profil.</span><span class="sxs-lookup"><span data-stu-id="081f9-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="081f9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="081f9-107">Parameters</span></span>

 <span data-ttu-id="081f9-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="081f9-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="081f9-109">[in] Ein Zeiger auf den Namen des Profils, das Kennwort zu ändernden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="081f9-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="081f9-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="081f9-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="081f9-111">[in] Ein Zeiger auf das aktuelle Kennwort.</span><span class="sxs-lookup"><span data-stu-id="081f9-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="081f9-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="081f9-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="081f9-113">[in] Ein Zeiger auf das neue Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="081f9-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="081f9-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="081f9-114">_ulFlags_</span></span>
  
> <span data-ttu-id="081f9-115">[in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="081f9-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="081f9-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="081f9-116">The following flag can be set:</span></span>
    
<span data-ttu-id="081f9-117">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="081f9-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="081f9-118">Der Name der Benutzerprofildienst und Kennwörter werden im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="081f9-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="081f9-119">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="081f9-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="081f9-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="081f9-120">Return value</span></span>

<span data-ttu-id="081f9-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="081f9-121">S_OK</span></span> 
  
> <span data-ttu-id="081f9-122">Wenn diese Methode aufgerufen wird, wird S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="081f9-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="081f9-123">Es wird jedoch keine Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="081f9-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="081f9-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="081f9-124">Remarks</span></span>

<span data-ttu-id="081f9-125">Verwenden Sie diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="081f9-125">Do not use this method.</span></span> <span data-ttu-id="081f9-126">MAPI unterstützt keine Kennwörter für Profile.</span><span class="sxs-lookup"><span data-stu-id="081f9-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="081f9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="081f9-127">See also</span></span>



[<span data-ttu-id="081f9-128">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="081f9-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

