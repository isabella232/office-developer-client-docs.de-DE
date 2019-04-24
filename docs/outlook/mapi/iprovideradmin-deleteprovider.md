---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279549"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="afff5-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="afff5-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="afff5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afff5-105">Löscht einen Dienstanbieter aus dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="afff5-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="afff5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afff5-106">Parameters</span></span>

 <span data-ttu-id="afff5-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="afff5-107">_lpUID_</span></span>
  
> <span data-ttu-id="afff5-108">[in, out] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner enthält, der den zu löschenden Anbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="afff5-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="afff5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afff5-109">Return value</span></span>

<span data-ttu-id="afff5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="afff5-110">S_OK</span></span> 
  
> <span data-ttu-id="afff5-111">Der Anbieter wurde erfolgreich aus dem Nachrichtendienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="afff5-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="afff5-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="afff5-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="afff5-113">Die **MAPIUID** , auf die durch den _lpUID_ -Parameter verwiesen wurde, wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="afff5-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="afff5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afff5-114">Remarks</span></span>

<span data-ttu-id="afff5-115">Mit der **IProviderAdmin::D eleteprovider** -Methode wird ein Dienstanbieter aus dem Nachrichtendienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="afff5-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="afff5-116">**DeleteProvider** bestimmt den zu löschenden Dienstanbieter, indem er der **MAPIUID** -Struktur entspricht, auf die durch _lpUID_ mit den von den aktiven Dienstanbietern registrierten Bezeichnern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="afff5-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="afff5-117">Bei den meisten Nachrichtendiensten können Anbieter nicht gelöscht werden, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="afff5-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="afff5-118">Wenn der zu löschende Anbieter verwendet wird, markiert **DeleteProvider** ihn zum Löschen, statt ihn sofort zu entfernen und S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="afff5-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="afff5-119">Wenn der Anbieter nicht mehr verwendet wird, wird er gelöscht.</span><span class="sxs-lookup"><span data-stu-id="afff5-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="afff5-120">**DeleteProvider** Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, bevor der Anbieter aus dem Dienst entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="afff5-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="afff5-121">Der Parameter _ulContext_ ist auf MSG_SERVICE_PROVIDER_DELETE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="afff5-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="afff5-122">Die Nachrichtendienst-Einstiegspunktfunktion führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="afff5-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="afff5-123">Löscht den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="afff5-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="afff5-124">Löscht den Profil Abschnitt des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="afff5-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="afff5-125">Die Nachrichtendienst-Einstiegspunktfunktion wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="afff5-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="afff5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afff5-126">See also</span></span>



[<span data-ttu-id="afff5-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="afff5-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="afff5-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="afff5-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="afff5-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="afff5-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

