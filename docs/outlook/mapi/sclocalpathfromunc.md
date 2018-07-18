---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795456"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="128c4-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="128c4-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="128c4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="128c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="128c4-105">Sucht nach einem Gegenstück lokaler Pfad zu dem angegebenen Pfad universal naming Convention (UNC).</span><span class="sxs-lookup"><span data-stu-id="128c4-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="128c4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="128c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="128c4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="128c4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="128c4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="128c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="128c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="128c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="128c4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="128c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="128c4-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="128c4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="128c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="128c4-112">Parameters</span></span>

 <span data-ttu-id="128c4-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="128c4-113">_szUNC_</span></span>
  
> <span data-ttu-id="128c4-114">[in] Einen Pfad im Format \\[ _Server_]\[ _Freigeben_]\[ _Pfad_] einer Datei oder ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="128c4-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="128c4-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="128c4-115">_szLocal_</span></span>
  
> <span data-ttu-id="128c4-116">[out] Einen Pfad im Format [ _Laufwerk:_]\[ _Pfad_] der gleichen Datei oder des Verzeichnisses wie bei der _SzUNC_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="128c4-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="128c4-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="128c4-117">_cchLocal_</span></span>
  
> <span data-ttu-id="128c4-118">[in] Die Größe des Puffers für die Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="128c4-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="128c4-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="128c4-119">Return value</span></span>

<span data-ttu-id="128c4-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="128c4-120">S_OK</span></span>
  
> <span data-ttu-id="128c4-121">Lokaler Pfad wurde erfolgreich gefunden.</span><span class="sxs-lookup"><span data-stu-id="128c4-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="128c4-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="128c4-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="128c4-123">_SzLocal_ war nicht groß genug für das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="128c4-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="128c4-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="128c4-124">S_FALSE</span></span>
  
> <span data-ttu-id="128c4-125">Die Zeichenfolge UNC war bereits ein lokaler Pfad.</span><span class="sxs-lookup"><span data-stu-id="128c4-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="128c4-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="128c4-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="128c4-127">Lokaler Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="128c4-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="128c4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="128c4-128">See also</span></span>



[<span data-ttu-id="128c4-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="128c4-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

