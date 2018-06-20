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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792339"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="8bdf6-103">IMAPIStatus:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="8bdf6-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="8bdf6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8bdf6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8bdf6-105">Ändert das Kennwort des Dienstanbieters ohne eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="8bdf6-106">Diese Methode ist optional in Status-Objekten unterstützt, mit denen Dienstanbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8bdf6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bdf6-107">Parameters</span></span>

 <span data-ttu-id="8bdf6-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="8bdf6-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="8bdf6-109">[in] Ein Zeiger auf das alte Kennwort.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="8bdf6-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="8bdf6-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="8bdf6-111">[in] Ein Zeiger auf das neue Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="8bdf6-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8bdf6-112">_ulFlags_</span></span>
  
> <span data-ttu-id="8bdf6-113">[in] Eine Bitmaske aus Flags, die das Format der Kennwörter steuert.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="8bdf6-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8bdf6-114">The following flag can be set:</span></span>
    
<span data-ttu-id="8bdf6-115">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8bdf6-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8bdf6-116">Die Kennwörter sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="8bdf6-117">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Kennwörter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bdf6-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8bdf6-118">Return value</span></span>

<span data-ttu-id="8bdf6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bdf6-119">S_OK</span></span> 
  
> <span data-ttu-id="8bdf6-120">Die Änderung des Kennworts erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-120">The password modification was successful.</span></span>
    
<span data-ttu-id="8bdf6-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8bdf6-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8bdf6-122">Das alte Kennwort auf den _LpOldPass_ ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="8bdf6-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8bdf6-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8bdf6-124">Das Statusobjekt unterstützt keine dieser Vorgang, wie durch die Abwesenheit des STATUS_CHANGE_PASSWORD-Flags in den Status des Objekts **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bdf6-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bdf6-125">Remarks</span></span>

<span data-ttu-id="8bdf6-126">Nicht alle Status Objekte unterstützen die **IMAPIStatus:: ChangePassword** -Methode.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="8bdf6-127">Es wird nur von Dienstanbietern unterstützt, die Clients ein Kennwort eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="8bdf6-128">Keines der Status, die von MAPI implementierte Objekte unterstützt die Operation Kennwort ändern.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="8bdf6-129">**ChangePassword** ändert ein Kennwort programmgesteuert ohne Benutzereingriff aus.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8bdf6-130">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8bdf6-130">Notes to implementers</span></span>

<span data-ttu-id="8bdf6-131">Remote-Transport-Anbieter implementieren **ChangePassword** gemäß hier.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="8bdf6-132">Es gibt keine besondere Aspekte.</span><span class="sxs-lookup"><span data-stu-id="8bdf6-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bdf6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bdf6-133">See also</span></span>



[<span data-ttu-id="8bdf6-134">Kanonische PidTagResourceMethods-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8bdf6-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="8bdf6-135">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8bdf6-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

