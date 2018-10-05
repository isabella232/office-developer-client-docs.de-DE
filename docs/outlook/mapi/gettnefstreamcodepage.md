---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399655"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="edd51-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="edd51-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="edd51-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edd51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edd51-105">Bestimmt die Codepage eines Streams Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="edd51-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edd51-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="edd51-106">Header file:</span></span>  <br/> |<span data-ttu-id="edd51-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="edd51-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="edd51-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="edd51-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="edd51-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="edd51-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="edd51-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="edd51-110">Called by:</span></span>  <br/> |<span data-ttu-id="edd51-111">Clientanwendungen und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="edd51-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="edd51-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="edd51-112">Parameters</span></span>

 <span data-ttu-id="edd51-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="edd51-113">_lpStream_</span></span>
  
> <span data-ttu-id="edd51-114">[in] Zeiger auf eine Speicher Stream-Objekt OLE **IStream** Schnittstelle, die beim Bereitstellen einer Datenquelle für eine TNEF-Nachricht Stream.</span><span class="sxs-lookup"><span data-stu-id="edd51-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="edd51-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="edd51-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="edd51-116">[out] Zeiger auf die Codepage des Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="edd51-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="edd51-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="edd51-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="edd51-118">[out] Zeiger auf der Seite Subcode des Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="edd51-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edd51-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edd51-119">Return value</span></span>

 <span data-ttu-id="edd51-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="edd51-120">**S_OK**</span></span>
  
> <span data-ttu-id="edd51-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="edd51-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="edd51-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="edd51-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="edd51-123">Es wurde ein Fehler beim Lesen eines Attributs in der TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="edd51-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="edd51-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="edd51-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="edd51-125">Entweder der Stream war nicht TNEF-Stream, oder es wurde ein Fehler beim Lesen des AttOemCodepage-Attributs.</span><span class="sxs-lookup"><span data-stu-id="edd51-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edd51-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edd51-126">Remarks</span></span>

<span data-ttu-id="edd51-127">Verwenden Sie die **GetTnefStreamCodepage** -Funktion, um das **AttOemCodepage** -Attribut des Datenstroms TNEF zum Bestimmen der Codepage und Subcode Seite lesen.</span><span class="sxs-lookup"><span data-stu-id="edd51-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="edd51-128">Wenn **AttOemCodepage** nicht gefunden wird, gibt **GetTnefStreamCodepage** Codepage 437 und einer Seite Subcode 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="edd51-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="edd51-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd51-129">See also</span></span>



[<span data-ttu-id="edd51-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="edd51-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

