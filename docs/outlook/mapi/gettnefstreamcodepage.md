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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299433"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="822de-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="822de-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="822de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="822de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="822de-105">Bestimmt die Codeseite für einen Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="822de-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="822de-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="822de-106">Header file:</span></span>  <br/> |<span data-ttu-id="822de-107">tnef.h</span><span class="sxs-lookup"><span data-stu-id="822de-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="822de-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="822de-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="822de-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="822de-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="822de-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="822de-110">Called by:</span></span>  <br/> |<span data-ttu-id="822de-111">Clientanwendungen und Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="822de-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="822de-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="822de-112">Parameters</span></span>

 <span data-ttu-id="822de-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="822de-113">_lpStream_</span></span>
  
> <span data-ttu-id="822de-114">[in] Zeiger auf eine OLE **IStream-Schnittstelle** des Speicherdatenstromobjekts, die eine Quelle für eine TNEF-Streamnachricht bietet.</span><span class="sxs-lookup"><span data-stu-id="822de-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="822de-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="822de-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="822de-116">[out] Zeiger auf die Codeseite des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="822de-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="822de-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="822de-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="822de-118">[out] Zeiger auf die Untercodeseite des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="822de-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="822de-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="822de-119">Return value</span></span>

 <span data-ttu-id="822de-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="822de-120">**S_OK**</span></span>
  
> <span data-ttu-id="822de-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="822de-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="822de-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="822de-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="822de-123">Fehler beim Lesen eines Attributs im TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="822de-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="822de-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="822de-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="822de-125">Entweder war der Datenstrom kein TNEF-Stream, oder es ist ein Fehler beim Lesen des attOemCodepage-Attributs aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="822de-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="822de-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="822de-126">Remarks</span></span>

<span data-ttu-id="822de-127">Verwenden Sie **die GetTnefStreamCodepage-Funktion,** um das **attOemCodepage-Attribut** des TNEF-Datenstroms zu lesen, um die Codeseite und die Untercodeseite zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="822de-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="822de-128">Wenn **attOemCodepage** nicht gefunden wird, gibt **GetTnefStreamCodepage** eine Codeseite von 437 und eine Untercodeseite von 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="822de-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="822de-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="822de-129">See also</span></span>



[<span data-ttu-id="822de-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="822de-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

