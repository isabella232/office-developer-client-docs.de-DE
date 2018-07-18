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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01cc8a8a54137b72091abab3671c08b526ef9e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792795"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="5b242-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="5b242-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="5b242-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b242-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b242-105">Fügt einen Dienstanbieter an den Dienst.</span><span class="sxs-lookup"><span data-stu-id="5b242-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="5b242-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b242-106">Parameters</span></span>

 <span data-ttu-id="5b242-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="5b242-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="5b242-108">[in] Ein Zeiger auf den Namen des hinzuzufügenden Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="5b242-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="5b242-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="5b242-109">_cValues_</span></span>
  
> <span data-ttu-id="5b242-110">[in] Die Anzahl der Eigenschaftswerte, die auf den durch den Parameter _LpProps_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="5b242-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="5b242-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="5b242-111">_lpProps_</span></span>
  
> <span data-ttu-id="5b242-112">[in] Ein Zeiger auf ein Array-Eigenschaft Wert, der beschreibt die Eigenschaften des hinzuzufügenden Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="5b242-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="5b242-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5b242-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5b242-114">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="5b242-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="5b242-115">Der Parameter _UlUIParam_ wird verwendet, wenn das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b242-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="5b242-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b242-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5b242-117">[in] Eine Bitmaske aus Flags, die die hinzugefügte Anbieter steuert.</span><span class="sxs-lookup"><span data-stu-id="5b242-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="5b242-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5b242-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="5b242-119">MAPI_DIALOG: Zeigt ein Dialogfeld Informationen zur Konfiguration aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="5b242-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="5b242-120">Parameter MAPI_UNICODE: Anbieter für die Eigenschaften Name und die Zeichenfolge sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="5b242-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="5b242-121">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="5b242-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5b242-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5b242-122">_lpUID_</span></span>
  
> <span data-ttu-id="5b242-123">[out] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner, der den Anbieter enthält hinzufügen darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b242-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5b242-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5b242-124">Return value</span></span>

<span data-ttu-id="5b242-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b242-125">S_OK</span></span> 
  
> <span data-ttu-id="5b242-126">Der Anbieter wurde erfolgreich an den Nachrichtendienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b242-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="5b242-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5b242-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5b242-128">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5b242-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5b242-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b242-129">Remarks</span></span>

<span data-ttu-id="5b242-130">Die **IProviderAdmin::CreateProvider** -Methode hinzugefügt der Messagingdiensts einen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="5b242-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="5b242-131">Der Parameter _LpszProvider_ muss auf den Namen eines Anbieters zeigen, die den Dienst gehört.</span><span class="sxs-lookup"><span data-stu-id="5b242-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="5b242-132">**CreateProvider** überprüft nicht, ob der Name des Anbieters in den Dienst mit dem Namen übereinstimmt; Wenn der übergebene Name den Namen eines Dienstes nicht übereinstimmt, der Aufruf erfolgreich ist, aber sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="5b242-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="5b242-133">Die meisten Message-Dienste können nicht Anbieter hinzugefügt oder gelöscht werden, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b242-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="5b242-134">Nachdem alle verfügbaren Informationen über den Dienst wurde Anbieter hinzugefügt das Profil aus der Datei "Mapisvc.inf" **CreateProvider** die Messagingdiensts Eintrag Punkt mit der _UlContext_ -Parameter auf MSG_SERVICE_ Funktionsaufrufe PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="5b242-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="5b242-135">Wenn in der **CreateProvider** -Methode _UlFlags_ Parameter MAPI_DIALOG festgelegt ist, werden die Werte in den _UlUIParam_ und _UlFlags_ auch an die Eintrags-Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="5b242-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="5b242-136">Aktivieren Sie diese zusätzlichen Parameter des-Dienstanbieters für das Eigenschaftenfenster anzuzeigen, damit der Benutzer Konfigurationseinstellungen eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="5b242-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b242-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b242-137">See also</span></span>

- [<span data-ttu-id="5b242-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5b242-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="5b242-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="5b242-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="5b242-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5b242-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="5b242-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b242-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

