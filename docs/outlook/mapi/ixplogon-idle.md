---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792876"
---
# <a name="ixplogonidle"></a><span data-ttu-id="03ff6-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="03ff6-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="03ff6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03ff6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03ff6-105">Gibt an, dass das System im Leerlauf, der Adressbuchhierarchie niedriger Priorität Operationen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="03ff6-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="03ff6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ff6-106">Parameters</span></span>

 <span data-ttu-id="03ff6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03ff6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="03ff6-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="03ff6-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03ff6-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="03ff6-109">Return value</span></span>

<span data-ttu-id="03ff6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="03ff6-110">S_OK</span></span> 
  
> <span data-ttu-id="03ff6-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03ff6-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03ff6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03ff6-112">Remarks</span></span>

<span data-ttu-id="03ff6-113">Die MAPI-Warteschlange ruft in regelmäßigen Abständen die **IXPLogon::Idle** -Methode, wenn Zeiten angefordert, wenn das System ist, indem das Flag XP_LOGON_SP im Aufruf der [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode, die die aktuelle Sitzung geöffnet übergeben im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="03ff6-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="03ff6-114">Bisweilen, wenn das System im Leerlauf befindet, kann der Adressbuchhierarchie Hintergrundvorgängen ausgeführt werden, die nicht richtig sind bei anderen anrufen oder, die in regelmäßigen Abständen auftreten, müssen.</span><span class="sxs-lookup"><span data-stu-id="03ff6-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03ff6-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ff6-115">See also</span></span>



[<span data-ttu-id="03ff6-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="03ff6-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="03ff6-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03ff6-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

