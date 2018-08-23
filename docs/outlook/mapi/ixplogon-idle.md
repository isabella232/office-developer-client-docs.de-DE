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
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578012"
---
# <a name="ixplogonidle"></a><span data-ttu-id="aa102-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="aa102-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="aa102-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa102-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa102-105">Gibt an, dass das System im Leerlauf, der Adressbuchhierarchie niedriger Priorität Operationen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="aa102-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aa102-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa102-106">Parameters</span></span>

 <span data-ttu-id="aa102-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa102-107">_ulFlags_</span></span>
  
> <span data-ttu-id="aa102-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="aa102-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa102-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="aa102-109">Return value</span></span>

<span data-ttu-id="aa102-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa102-110">S_OK</span></span> 
  
> <span data-ttu-id="aa102-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa102-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa102-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="aa102-112">Remarks</span></span>

<span data-ttu-id="aa102-113">Die MAPI-Warteschlange ruft in regelmäßigen Abständen die **IXPLogon::Idle** -Methode, wenn Zeiten angefordert, wenn das System ist, indem das Flag XP_LOGON_SP im Aufruf der [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode, die die aktuelle Sitzung geöffnet übergeben im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="aa102-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="aa102-114">Bisweilen, wenn das System im Leerlauf befindet, kann der Adressbuchhierarchie Hintergrundvorgängen ausgeführt werden, die nicht richtig sind bei anderen anrufen oder, die in regelmäßigen Abständen auftreten, müssen.</span><span class="sxs-lookup"><span data-stu-id="aa102-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa102-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa102-115">See also</span></span>



[<span data-ttu-id="aa102-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="aa102-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="aa102-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa102-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

