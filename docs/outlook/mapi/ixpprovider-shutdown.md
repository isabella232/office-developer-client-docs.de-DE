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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792887"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="23e7c-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="23e7c-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="23e7c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23e7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23e7c-105">In einer bestimmten Reihenfolge eines Transportdienstes wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="23e7c-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="23e7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23e7c-106">Parameters</span></span>

 <span data-ttu-id="23e7c-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="23e7c-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="23e7c-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="23e7c-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23e7c-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="23e7c-109">Return value</span></span>

<span data-ttu-id="23e7c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="23e7c-110">S_OK</span></span> 
  
> <span data-ttu-id="23e7c-111">Der Anruf in der Adressbuchhierarchie heruntergefahren war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="23e7c-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23e7c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e7c-112">Remarks</span></span>

<span data-ttu-id="23e7c-113">Die MAPI-Warteschlange Ruft die **IXPProvider::Shutdown** -Methode unmittelbar vor der Freigabe ein Transport-Anbieter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="23e7c-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="23e7c-114">Vor dem **Herunterfahren**aufrufen, gibt MAPI alle Logon-Objekten für einen Anbieter frei.</span><span class="sxs-lookup"><span data-stu-id="23e7c-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23e7c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23e7c-115">See also</span></span>



[<span data-ttu-id="23e7c-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="23e7c-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="23e7c-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23e7c-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

