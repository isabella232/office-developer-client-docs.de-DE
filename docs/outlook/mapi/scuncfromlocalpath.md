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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590106"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="87e80-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="87e80-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="87e80-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87e80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87e80-105">Sucht nach einer universal naming Convention (UNC) Pfad Entsprechung für den angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="87e80-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87e80-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="87e80-106">Header file:</span></span>  <br/> |<span data-ttu-id="87e80-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87e80-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="87e80-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="87e80-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="87e80-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="87e80-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="87e80-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="87e80-110">Called by:</span></span>  <br/> |<span data-ttu-id="87e80-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="87e80-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="87e80-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87e80-112">Parameters</span></span>

 <span data-ttu-id="87e80-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="87e80-113">_szLocal_</span></span>
  
> <span data-ttu-id="87e80-114">[in] Einen Pfad im Format [ _Laufwerk:_]\[ _Pfad_] einer Datei oder ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="87e80-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="87e80-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="87e80-115">_szUNC_</span></span>
  
> <span data-ttu-id="87e80-116">[out] Einen Pfad im Format \\[ _Server_]\[ _Freigeben_]\[ _Pfad_] der gleichen Datei oder des Verzeichnisses wie bei der _SzLocal_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="87e80-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="87e80-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="87e80-117">_cchUNC_</span></span>
  
> <span data-ttu-id="87e80-118">[in] Die Größe des Puffers für die Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="87e80-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87e80-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="87e80-119">Return value</span></span>

<span data-ttu-id="87e80-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="87e80-120">S_OK</span></span>
  
> <span data-ttu-id="87e80-121">Das Gegenstück der UNC-Pfad wurde erfolgreich gefunden.</span><span class="sxs-lookup"><span data-stu-id="87e80-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="87e80-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87e80-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="87e80-123">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="87e80-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="87e80-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="87e80-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="87e80-125">_SzUNC_ war nicht groß genug für das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="87e80-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="87e80-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="87e80-126">S_FALSE</span></span>
  
> <span data-ttu-id="87e80-127">Der lokale Pfad wurde bereits eine UNC-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="87e80-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87e80-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87e80-128">See also</span></span>



[<span data-ttu-id="87e80-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="87e80-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

