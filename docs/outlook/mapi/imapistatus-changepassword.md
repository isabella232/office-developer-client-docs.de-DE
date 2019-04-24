---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328280"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="7b6fa-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="7b6fa-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="7b6fa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b6fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b6fa-105">Ändert das Kennwort eines Dienstanbieters, ohne eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="7b6fa-106">Diese Methode wird optional in Status-Objekten unterstützt, die von Dienstanbietern implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7b6fa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b6fa-107">Parameters</span></span>

 <span data-ttu-id="7b6fa-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="7b6fa-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="7b6fa-109">in Ein Zeiger auf das alte Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="7b6fa-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="7b6fa-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="7b6fa-111">in Ein Zeiger auf das neue Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="7b6fa-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7b6fa-112">_ulFlags_</span></span>
  
> <span data-ttu-id="7b6fa-113">in Eine Bitmaske von Flags, die das Format der Kennwörter steuert.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="7b6fa-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7b6fa-114">The following flag can be set:</span></span>
    
<span data-ttu-id="7b6fa-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b6fa-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7b6fa-116">Die Kennwörter sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="7b6fa-117">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Kennwörter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b6fa-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b6fa-118">Return value</span></span>

<span data-ttu-id="7b6fa-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b6fa-119">S_OK</span></span> 
  
> <span data-ttu-id="7b6fa-120">Die Kennwortänderung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-120">The password modification was successful.</span></span>
    
<span data-ttu-id="7b6fa-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7b6fa-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7b6fa-122">Das alte Kennwort, auf das durch _lpOldPass_ verwiesen wird, ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="7b6fa-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7b6fa-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7b6fa-124">Das Status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_CHANGE_PASSWORD-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Status-Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b6fa-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b6fa-125">Remarks</span></span>

<span data-ttu-id="7b6fa-126">Nicht alle Status-Objekte unterstützen die **IMAPIStatus:: ChangePassword** -Methode.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="7b6fa-127">Er wird nur von Dienstanbietern unterstützt, für die Clients ein Kennwort eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="7b6fa-128">Keines der von MAPI implementierten Statusobjekte unterstützt den Vorgang der Kennwortänderung.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="7b6fa-129">**ChangePassword** ändert ein Kennwort programmgesteuert ohne Benutzereingriff.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b6fa-130">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7b6fa-130">Notes to implementers</span></span>

<span data-ttu-id="7b6fa-131">Remote Transportanbieter implementieren **ChangePassword** wie hier angegeben.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="7b6fa-132">Besondere Überlegungen sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="7b6fa-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b6fa-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b6fa-133">See also</span></span>



[<span data-ttu-id="7b6fa-134">Kanonische Pidtagresourcemethods (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b6fa-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="7b6fa-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7b6fa-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

