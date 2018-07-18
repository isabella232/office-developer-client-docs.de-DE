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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792675"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="8e33a-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="8e33a-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="8e33a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e33a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e33a-105">Schließt einen Anbieter für Nachricht Anmelden in einer bestimmten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8e33a-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8e33a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e33a-106">Parameters</span></span>

 <span data-ttu-id="8e33a-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e33a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8e33a-108">[in] Reserviert. Ein Zeiger auf 0 (null) muss sein.</span><span class="sxs-lookup"><span data-stu-id="8e33a-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e33a-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8e33a-109">Return value</span></span>

<span data-ttu-id="8e33a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e33a-110">S_OK</span></span> 
  
> <span data-ttu-id="8e33a-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e33a-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e33a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e33a-112">Remarks</span></span>

<span data-ttu-id="8e33a-113">MAPI-Aufrufen die **IMSProvider::Shutdown** -Methode unmittelbar vor der Freigabe des Message-Speicher-Anbieter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8e33a-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="8e33a-114">MAPI-Freigaben für alle Logon-Objekten für einen Anbieter vor dem **Herunterfahren** für diesen Anbieter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8e33a-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e33a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e33a-115">See also</span></span>



[<span data-ttu-id="8e33a-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e33a-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

