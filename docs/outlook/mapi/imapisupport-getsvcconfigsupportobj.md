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
ms.openlocfilehash: 1c48ceefa84658b236b8dfa4e10df18c175d920e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595160"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="19808-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="19808-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="19808-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19808-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19808-105">Erstellt ein Objekt "Message" Service Support.</span><span class="sxs-lookup"><span data-stu-id="19808-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="19808-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19808-106">Parameters</span></span>

 <span data-ttu-id="19808-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19808-107">_ulFlags_</span></span>
  
> <span data-ttu-id="19808-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="19808-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="19808-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="19808-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="19808-110">[out] Ein Zeiger auf einen Zeiger auf das neue Nachricht Support-Objekt.</span><span class="sxs-lookup"><span data-stu-id="19808-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19808-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="19808-111">Return value</span></span>

<span data-ttu-id="19808-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="19808-112">S_OK</span></span> 
  
> <span data-ttu-id="19808-113">Das Support-Konfigurationsobjekt wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="19808-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19808-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="19808-114">Remarks</span></span>

<span data-ttu-id="19808-115">Die **IMAPISupport::GetSvcConfigSupportObj** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="19808-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="19808-116">Dienstanbieter anrufen **GetSvcConfigSupportObj** zum Erstellen eines Objekts Konfiguration Unterstützung, um auf eine Nachricht Service Entry Point-Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="19808-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="19808-117">Eine Nachricht Service Entry Point-Funktion basiert auf den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp und von Methoden der [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19808-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="19808-118">Eine Nachricht Service Entry Point-Funktion ermöglicht Message Dienste so konfigurieren selbst oder andere Aktionen durchführen, wenn das Profil geändert wird.</span><span class="sxs-lookup"><span data-stu-id="19808-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="19808-119">Nachricht Service-Einstiegspunkt, dass Funktionen konfigurationsänderungen unterstützen können durch Anzeigen eines Eigenschaftenblatts oder über ein Array-Eigenschaft Wert an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="19808-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19808-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19808-120">See also</span></span>



[<span data-ttu-id="19808-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19808-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="19808-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="19808-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="19808-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="19808-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="19808-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19808-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="19808-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="19808-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="19808-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="19808-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

