---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589091"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="44f87-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="44f87-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="44f87-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f87-105">Schließt einen Anbieter für Nachricht Anmelden in einer bestimmten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="44f87-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="44f87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44f87-106">Parameters</span></span>

 <span data-ttu-id="44f87-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="44f87-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="44f87-108">[in] Reserviert. Ein Zeiger auf 0 (null) muss sein.</span><span class="sxs-lookup"><span data-stu-id="44f87-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="44f87-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="44f87-109">Return value</span></span>

<span data-ttu-id="44f87-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="44f87-110">S_OK</span></span> 
  
> <span data-ttu-id="44f87-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44f87-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44f87-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="44f87-112">Remarks</span></span>

<span data-ttu-id="44f87-113">MAPI-Aufrufen die **IMSProvider::Shutdown** -Methode unmittelbar vor der Freigabe des Message-Speicher-Anbieter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="44f87-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="44f87-114">MAPI-Freigaben für alle Logon-Objekten für einen Anbieter vor dem **Herunterfahren** für diesen Anbieter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44f87-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44f87-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44f87-115">See also</span></span>



[<span data-ttu-id="44f87-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44f87-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

