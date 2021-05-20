---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430805"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="a258c-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="a258c-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="a258c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a258c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a258c-105">Fügt dem Nachrichtendienst einen Dienstanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="a258c-105">Adds a service provider to the message service.</span></span> 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="a258c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a258c-106">Parameters</span></span>

 <span data-ttu-id="a258c-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="a258c-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="a258c-108">[in] Ein Zeiger auf den Namen des hinzuzufügende Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a258c-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="a258c-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="a258c-109">_cValues_</span></span>
  
> <span data-ttu-id="a258c-110">[in] Die Anzahl der Eigenschaftswerte, auf die der  _lpProps-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="a258c-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="a258c-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="a258c-111">_lpProps_</span></span>
  
> <span data-ttu-id="a258c-112">[in] Ein Zeiger auf ein Eigenschaftenwertarray, das die Eigenschaften des hinzuzufügenden Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a258c-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="a258c-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a258c-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="a258c-114">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a258c-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="a258c-115">Der  _ulUIParam-Parameter_ wird verwendet, wenn MAPI_DIALOG im  _ulFlags-Parameter festgelegt_ ist.</span><span class="sxs-lookup"><span data-stu-id="a258c-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a258c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a258c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a258c-117">[in] Eine Bitmaske mit Flags, die die Anbieter-Addition steuert.</span><span class="sxs-lookup"><span data-stu-id="a258c-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="a258c-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a258c-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="a258c-119">MAPI_DIALOG: Zeigt ein Dialogfeld an, in dem Konfigurationsinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a258c-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="a258c-120">MAPI_UNICODE: Der Anbietername und die Zeichenfolgeneigenschaften sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="a258c-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="a258c-121">Wenn das MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="a258c-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a258c-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="a258c-122">_lpUID_</span></span>
  
> <span data-ttu-id="a258c-123">[out] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, der den hinzuzufügenden Anbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="a258c-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a258c-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a258c-124">Return value</span></span>

<span data-ttu-id="a258c-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="a258c-125">S_OK</span></span> 
  
> <span data-ttu-id="a258c-126">Der Anbieter wurde erfolgreich dem Nachrichtendienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258c-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="a258c-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a258c-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a258c-128">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="a258c-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a258c-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a258c-129">Remarks</span></span>

<span data-ttu-id="a258c-130">Die **IProviderAdmin::CreateProvider-Methode** fügt dem Nachrichtendienst einen Dienstanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="a258c-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="a258c-131">Der  _lpszProvider-Parameter_ muss auf den Namen eines Anbieters verweisen, der zum Nachrichtendienst gehört.</span><span class="sxs-lookup"><span data-stu-id="a258c-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="a258c-132">**CreateProvider** überprüft nicht, ob der Name dem Namen eines Anbieters im Dienst entspricht. Wenn der übergebene Name nicht mit einem Dienstnamen übereinstimmen, ist der Aufruf erfolgreich, die Ergebnisse sind jedoch unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="a258c-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="a258c-133">Die meisten Nachrichtendienste ermöglichen das Hinzufügen oder Löschen von Anbietern während der Verwendung des Profils nicht.</span><span class="sxs-lookup"><span data-stu-id="a258c-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="a258c-134">Nachdem alle verfügbaren Informationen zum Dienstanbieter dem Profil aus der Datei Mapisvc.inf hinzugefügt wurden, ruft **CreateProvider** die Einstiegspunktfunktion des Nachrichtendiensts auf, und der  _ulContext-Parameter_ ist auf MSG_SERVICE_PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="a258c-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="a258c-135">Wenn MAPI_DIALOG im _ulFlags-Parameter_ der **CreateProvider-Methode** festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ ebenfalls an die Einstiegspunktfunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="a258c-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="a258c-136">Mit diesen zusätzlichen Parametern kann der Dienstanbieter sein Eigenschaftenblatt anzeigen, damit der Benutzer Konfigurationseinstellungen eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="a258c-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a258c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a258c-137">See also</span></span>

- [<span data-ttu-id="a258c-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a258c-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="a258c-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="a258c-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="a258c-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a258c-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="a258c-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a258c-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

