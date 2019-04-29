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
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438624"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="1d5fc-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="1d5fc-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="1d5fc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d5fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d5fc-105">Schließt einen Nachrichtenspeicher Anbieter ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1d5fc-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1d5fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d5fc-106">Parameters</span></span>

 <span data-ttu-id="1d5fc-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d5fc-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1d5fc-108">in Reserviert muss ein Zeiger auf NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1d5fc-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d5fc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d5fc-109">Return value</span></span>

<span data-ttu-id="1d5fc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d5fc-110">S_OK</span></span> 
  
> <span data-ttu-id="1d5fc-111">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1d5fc-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d5fc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d5fc-112">Remarks</span></span>

<span data-ttu-id="1d5fc-113">MAPI Ruft die **IMSProvider:: Shutdown** -Methode unmittelbar vor dem Freigeben des Nachrichtenspeicher-Anbieterobjekts auf.</span><span class="sxs-lookup"><span data-stu-id="1d5fc-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="1d5fc-114">MAPI gibt alle Anmeldeobjekte für einen Anbieter frei, bevor das **Herunterfahren** für diesen Anbieter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1d5fc-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d5fc-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d5fc-115">See also</span></span>



[<span data-ttu-id="1d5fc-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d5fc-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

