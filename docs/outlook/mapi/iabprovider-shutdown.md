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
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567888"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="68858-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="68858-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="68858-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68858-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68858-105">Bricht eine Verbindung mit einer aktiven Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="68858-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="68858-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68858-106">Parameters</span></span>

 <span data-ttu-id="68858-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="68858-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="68858-108">[In] Reserviert. Ein Zeiger auf 0 (null) muss sein.</span><span class="sxs-lookup"><span data-stu-id="68858-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68858-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="68858-109">Return value</span></span>

<span data-ttu-id="68858-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="68858-110">S_OK</span></span> 
  
> <span data-ttu-id="68858-111">Die Verbindung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="68858-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="68858-112">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="68858-112">Notes to implementers</span></span>

<span data-ttu-id="68858-113">Führen Sie in der Implementierung der **Shutdown** -Methode jegliches Aufgaben erforderlich werden sollten.</span><span class="sxs-lookup"><span data-stu-id="68858-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="68858-114">MAPI-Aufrufen **Shutdown** -Methode nur, nachdem Sie alle Objekte Ihrer Anmeldung freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="68858-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68858-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68858-115">See also</span></span>



[<span data-ttu-id="68858-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68858-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

