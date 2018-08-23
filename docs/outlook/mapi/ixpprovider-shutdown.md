---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592605"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="194de-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="194de-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="194de-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="194de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="194de-105">In einer bestimmten Reihenfolge eines Transportdienstes wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="194de-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="194de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="194de-106">Parameters</span></span>

 <span data-ttu-id="194de-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="194de-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="194de-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="194de-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="194de-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="194de-109">Return value</span></span>

<span data-ttu-id="194de-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="194de-110">S_OK</span></span> 
  
> <span data-ttu-id="194de-111">Der Anruf in der Adressbuchhierarchie heruntergefahren war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="194de-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="194de-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="194de-112">Remarks</span></span>

<span data-ttu-id="194de-113">Die MAPI-Warteschlange Ruft die **IXPProvider::Shutdown** -Methode unmittelbar vor der Freigabe ein Transport-Anbieter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="194de-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="194de-114">Vor dem **Herunterfahren**aufrufen, gibt MAPI alle Logon-Objekten für einen Anbieter frei.</span><span class="sxs-lookup"><span data-stu-id="194de-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="194de-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="194de-115">See also</span></span>



[<span data-ttu-id="194de-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="194de-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="194de-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="194de-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

