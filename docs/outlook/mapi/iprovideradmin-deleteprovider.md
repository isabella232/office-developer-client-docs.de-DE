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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404862"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="81459-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="81459-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="81459-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81459-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81459-105">Löscht einen Dienstanbieter aus dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="81459-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="81459-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81459-106">Parameters</span></span>

 <span data-ttu-id="81459-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="81459-107">_lpUID_</span></span>
  
> <span data-ttu-id="81459-108">[in, out] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, der den zu löschenden Anbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="81459-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="81459-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81459-109">Return value</span></span>

<span data-ttu-id="81459-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="81459-110">S_OK</span></span> 
  
> <span data-ttu-id="81459-111">Der Anbieter wurde erfolgreich aus dem Nachrichtendienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="81459-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="81459-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="81459-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="81459-113">Die **MAPIUID,** auf die der  _lpUID-Parameter_ verweist, wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="81459-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="81459-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81459-114">Remarks</span></span>

<span data-ttu-id="81459-115">Die **IProviderAdmin::D eleteProvider-Methode** löscht einen Dienstanbieter aus dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="81459-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="81459-116">**DeleteProvider** bestimmt den zu löschenden Dienstanbieter, indem die **MAPIUID-Struktur,** auf die  _von lpUID_ verwiesen wird, mit dem Satz von Bezeichnern, die von den aktiven Dienstanbietern registriert wurden, übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="81459-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="81459-117">Die meisten Nachrichtendienste lassen das Löschen von Anbietern während der Verwendung des Profils nicht zu.</span><span class="sxs-lookup"><span data-stu-id="81459-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="81459-118">Wenn der zu löschende Anbieter verwendet wird, markiert **DeleteProvider** ihn zum Löschen, anstatt ihn sofort zu entfernen, und gibt S_OK.</span><span class="sxs-lookup"><span data-stu-id="81459-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="81459-119">Wenn der Anbieter nicht mehr verwendet wird, wird er gelöscht.</span><span class="sxs-lookup"><span data-stu-id="81459-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="81459-120">**DeleteProvider** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, bevor der Anbieter aus dem Dienst entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="81459-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="81459-121">Der  _ulContext-Parameter_ ist auf MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="81459-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="81459-122">Die Einstiegspunktfunktion des Nachrichtendiensts führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="81459-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="81459-123">Löscht den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="81459-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="81459-124">Löscht den Profilabschnitt des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="81459-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="81459-125">Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="81459-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81459-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81459-126">See also</span></span>



[<span data-ttu-id="81459-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="81459-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="81459-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="81459-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="81459-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81459-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

