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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339298"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="880cc-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="880cc-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="880cc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="880cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="880cc-105">Initiiert den ABMELDEPROZESS.</span><span class="sxs-lookup"><span data-stu-id="880cc-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="880cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="880cc-106">Parameters</span></span>

 <span data-ttu-id="880cc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="880cc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="880cc-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="880cc-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="880cc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="880cc-109">Return value</span></span>

<span data-ttu-id="880cc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="880cc-110">S_OK</span></span> 
  
> <span data-ttu-id="880cc-111">Der ABMELDEPROZESS wurde erfolgreich initiiert.</span><span class="sxs-lookup"><span data-stu-id="880cc-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="880cc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="880cc-112">Remarks</span></span>

<span data-ttu-id="880cc-113">Der ABMELDEPROZESS wird in der Regel gestartet, wenn ein Client die [IMAPISession:: Abmelde](imapisession-logoff.md) Methode aufruft, um eine Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="880cc-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="880cc-114">MAPI ruft dann die **IABLogon:: Abmelde** Methode jedes Adressbuch Anbieters auf, um den ABMELDEPROZESS zu starten.</span><span class="sxs-lookup"><span data-stu-id="880cc-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="880cc-115">Die **IABLogon:: Logout** -Methode führt die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="880cc-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="880cc-116">Gibt alle geöffneten Objekte wie alle unter Objekte oder das Status-Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="880cc-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="880cc-117">Gibt das Support Objekt des Anbieters frei.</span><span class="sxs-lookup"><span data-stu-id="880cc-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="880cc-118">Weitere Informationen zum ABMELDEPROZESS von Adressbuch Anbietern finden Sie unter [Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="880cc-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="880cc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="880cc-119">See also</span></span>



[<span data-ttu-id="880cc-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="880cc-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="880cc-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="880cc-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

