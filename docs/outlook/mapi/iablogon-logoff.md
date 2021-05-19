---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416398"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="1bf35-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="1bf35-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="1bf35-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bf35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bf35-105">Initiiert den Abmeldevorgang.</span><span class="sxs-lookup"><span data-stu-id="1bf35-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1bf35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bf35-106">Parameters</span></span>

 <span data-ttu-id="1bf35-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1bf35-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1bf35-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="1bf35-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1bf35-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bf35-109">Return value</span></span>

<span data-ttu-id="1bf35-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bf35-110">S_OK</span></span> 
  
> <span data-ttu-id="1bf35-111">Der Abmeldevorgang wurde erfolgreich initiiert.</span><span class="sxs-lookup"><span data-stu-id="1bf35-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1bf35-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1bf35-112">Remarks</span></span>

<span data-ttu-id="1bf35-113">Der Abmeldevorgang wird in der Regel gestartet, wenn ein Client die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft, um eine Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1bf35-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="1bf35-114">MAPI ruft dann die **IABLogon::Logoff-Methode** jedes Adressbuchanbieters auf, um den Abmeldevorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="1bf35-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="1bf35-115">Die **IABLogon::Logoff-Methode** führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1bf35-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="1bf35-116">Gibt alle geöffneten Objekte frei, z. B. alle Unterobjekte oder das Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="1bf35-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="1bf35-117">Gibt das Supportobjekt des Anbieters frei.</span><span class="sxs-lookup"><span data-stu-id="1bf35-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="1bf35-118">Weitere Informationen zum Abmeldevorgang von Adressbuchanbietern finden Sie unter [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1bf35-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1bf35-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bf35-119">See also</span></span>



[<span data-ttu-id="1bf35-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1bf35-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="1bf35-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bf35-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

