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
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409783"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="f0611-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="f0611-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="f0611-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0611-105">Bricht eine Verbindung zu einer aktiven Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="f0611-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f0611-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0611-106">Parameters</span></span>

 <span data-ttu-id="f0611-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0611-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f0611-108">[In] Reserviert; muss ein Zeiger auf Null sein.</span><span class="sxs-lookup"><span data-stu-id="f0611-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0611-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0611-109">Return value</span></span>

<span data-ttu-id="f0611-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0611-110">S_OK</span></span> 
  
> <span data-ttu-id="f0611-111">Die Verbindung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f0611-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="f0611-112">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f0611-112">Notes to implementers</span></span>

<span data-ttu-id="f0611-113">Führen Sie bei der Implementierung der **Shutdown-Methode** alle aufgaben aus, die Sie für erforderlich halten.</span><span class="sxs-lookup"><span data-stu-id="f0611-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="f0611-114">MAPI ruft Ihre **Shutdown-Methode** erst auf, nachdem Sie alle Anmeldeobjekte freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f0611-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0611-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0611-115">See also</span></span>



[<span data-ttu-id="f0611-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0611-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

