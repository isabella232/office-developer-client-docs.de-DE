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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791973"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="547d3-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="547d3-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="547d3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="547d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="547d3-105">Initiiert den Prozess abmelden.</span><span class="sxs-lookup"><span data-stu-id="547d3-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="547d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="547d3-106">Parameters</span></span>

 <span data-ttu-id="547d3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="547d3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="547d3-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="547d3-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="547d3-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="547d3-109">Return value</span></span>

<span data-ttu-id="547d3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="547d3-110">S_OK</span></span> 
  
> <span data-ttu-id="547d3-111">Der Prozess für die Abmeldung wurde erfolgreich initiiert.</span><span class="sxs-lookup"><span data-stu-id="547d3-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="547d3-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="547d3-112">Remarks</span></span>

<span data-ttu-id="547d3-113">Der Prozess für die Abmeldung wird in der Regel gestartet, wenn ein Client beenden eine Sitzung die [IMAPISession::Logoff](imapisession-logoff.md) Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="547d3-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="547d3-114">MAPI ruft dann jede Adressbuchanbieter **IABLogon::Logoff** -Methode, um den Abmeldung zu starten.</span><span class="sxs-lookup"><span data-stu-id="547d3-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="547d3-115">Die **IABLogon::Logoff** -Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="547d3-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="547d3-116">Gibt alle geöffneten Objekte, wie alle Unterobjekte oder das Statusobjekt frei.</span><span class="sxs-lookup"><span data-stu-id="547d3-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="547d3-117">Gibt den Anbieter DSO-Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="547d3-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="547d3-118">Weitere Informationen zum Abmeldevorgang, von adressbuchanbietern implementierte finden Sie unter [Herunterfahren nach unten a Service Provider](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="547d3-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="547d3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="547d3-119">See also</span></span>



[<span data-ttu-id="547d3-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="547d3-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="547d3-121">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="547d3-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

