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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436048"
---
# <a name="ixplogonidle"></a><span data-ttu-id="c8d05-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="c8d05-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="c8d05-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8d05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8d05-105">Gibt an, dass sich das System im Leerlauf befindet, sodass der Transportanbieter Vorgänge mit niedriger Priorität ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c8d05-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c8d05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8d05-106">Parameters</span></span>

 <span data-ttu-id="c8d05-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8d05-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c8d05-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="c8d05-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8d05-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8d05-109">Return value</span></span>

<span data-ttu-id="c8d05-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8d05-110">S_OK</span></span> 
  
> <span data-ttu-id="c8d05-111">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8d05-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8d05-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8d05-112">Remarks</span></span>

<span data-ttu-id="c8d05-113">Der MAPI-Spooler ruft die **IXPLogon::Idle-Methode** regelmäßig auf, wenn dies angefordert wird, wenn das System im Leerlauf ist, indem das flag XP_LOGON_SP im Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) übergeben wird, die die aktuelle Sitzung geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="c8d05-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="c8d05-114">In Zeiten, in denen sich das System im Leerlauf befindet, kann der Transportanbieter Hintergrundvorgänge ausführen, die bei anderen Anrufen nicht geeignet sind oder regelmäßig ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c8d05-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8d05-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d05-115">See also</span></span>



[<span data-ttu-id="c8d05-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="c8d05-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="c8d05-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8d05-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

