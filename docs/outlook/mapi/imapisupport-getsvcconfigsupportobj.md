---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411309"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="7043e-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="7043e-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="7043e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7043e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7043e-105">Erstellt ein Unterstützungsobjekt für den Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="7043e-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="7043e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7043e-106">Parameters</span></span>

 <span data-ttu-id="7043e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7043e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7043e-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7043e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7043e-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="7043e-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="7043e-110">[out] Ein Zeiger auf einen Zeiger auf das neue Unterstützungsobjekt des Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="7043e-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7043e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7043e-111">Return value</span></span>

<span data-ttu-id="7043e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7043e-112">S_OK</span></span> 
  
> <span data-ttu-id="7043e-113">Das Konfigurationsunterstützungsobjekt wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="7043e-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7043e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7043e-114">Remarks</span></span>

<span data-ttu-id="7043e-115">Die **IMAPISupport::GetSvcConfigSupportObj-Methode** wird für alle Supportobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="7043e-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="7043e-116">Dienstanbieter rufen **GetSvcConfigSupportObj** auf, um ein Konfigurationsunterstützungsobjekt zu erstellen, das an eine Nachrichtendienst-Einstiegspunktfunktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7043e-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="7043e-117">Eine Nachrichtendienst-Einstiegspunktfunktion basiert auf dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) und wird von Methoden der [IMsgServiceAdmin-Schnittstelle](imsgserviceadminiunknown.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7043e-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="7043e-118">Mit einer Nachrichtendienst-Einstiegspunktfunktion können Nachrichtendienste sich selbst konfigurieren oder andere Aktionen ausführen, wenn das Profil geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7043e-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="7043e-119">Nachrichtendienst-Einstiegspunktfunktionen können Konfigurationsänderungen unterstützen, indem ein Eigenschaftenblatt oder ein Eigenschaftswertarray angezeigt wird, das an die [IMsgServiceAdmin::ConfigureMsgService-Methode übergeben](imsgserviceadmin-configuremsgservice.md) wird.</span><span class="sxs-lookup"><span data-stu-id="7043e-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7043e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7043e-120">See also</span></span>



[<span data-ttu-id="7043e-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7043e-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="7043e-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="7043e-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="7043e-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="7043e-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="7043e-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7043e-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="7043e-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="7043e-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="7043e-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7043e-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

