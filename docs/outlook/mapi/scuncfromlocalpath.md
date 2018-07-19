---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795472"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="486d6-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="486d6-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="486d6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="486d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="486d6-105">Sucht nach einer universal naming Convention (UNC) Pfad Entsprechung für den angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="486d6-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="486d6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="486d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="486d6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="486d6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="486d6-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="486d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="486d6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="486d6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="486d6-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="486d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="486d6-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="486d6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="486d6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="486d6-112">Parameters</span></span>

 <span data-ttu-id="486d6-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="486d6-113">_szLocal_</span></span>
  
> <span data-ttu-id="486d6-114">[in] Einen Pfad im Format [ _Laufwerk:_]\[ _Pfad_] einer Datei oder ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="486d6-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="486d6-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="486d6-115">_szUNC_</span></span>
  
> <span data-ttu-id="486d6-116">[out] Einen Pfad im Format \\[ _Server_]\[ _Freigeben_]\[ _Pfad_] der gleichen Datei oder des Verzeichnisses wie bei der _SzLocal_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="486d6-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="486d6-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="486d6-117">_cchUNC_</span></span>
  
> <span data-ttu-id="486d6-118">[in] Die Größe des Puffers für die Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="486d6-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="486d6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="486d6-119">Return value</span></span>

<span data-ttu-id="486d6-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="486d6-120">S_OK</span></span>
  
> <span data-ttu-id="486d6-121">Das Gegenstück der UNC-Pfad wurde erfolgreich gefunden.</span><span class="sxs-lookup"><span data-stu-id="486d6-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="486d6-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="486d6-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="486d6-123">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="486d6-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="486d6-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="486d6-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="486d6-125">_SzUNC_ war nicht groß genug für das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="486d6-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="486d6-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="486d6-126">S_FALSE</span></span>
  
> <span data-ttu-id="486d6-127">Der lokale Pfad wurde bereits eine UNC-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="486d6-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="486d6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="486d6-128">See also</span></span>



[<span data-ttu-id="486d6-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="486d6-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

