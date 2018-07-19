---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791990"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="c79ba-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="c79ba-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="c79ba-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c79ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c79ba-105">Bricht eine Verbindung mit einer aktiven Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="c79ba-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c79ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c79ba-106">Parameters</span></span>

 <span data-ttu-id="c79ba-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="c79ba-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="c79ba-108">[In] Reserviert. Ein Zeiger auf 0 (null) muss sein.</span><span class="sxs-lookup"><span data-stu-id="c79ba-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c79ba-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c79ba-109">Return value</span></span>

<span data-ttu-id="c79ba-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c79ba-110">S_OK</span></span> 
  
> <span data-ttu-id="c79ba-111">Die Verbindung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c79ba-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c79ba-112">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c79ba-112">Notes to implementers</span></span>

<span data-ttu-id="c79ba-113">Führen Sie in der Implementierung der **Shutdown** -Methode jegliches Aufgaben erforderlich werden sollten.</span><span class="sxs-lookup"><span data-stu-id="c79ba-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="c79ba-114">MAPI-Aufrufen **Shutdown** -Methode nur, nachdem Sie alle Objekte Ihrer Anmeldung freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c79ba-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c79ba-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c79ba-115">See also</span></span>



[<span data-ttu-id="c79ba-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c79ba-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

