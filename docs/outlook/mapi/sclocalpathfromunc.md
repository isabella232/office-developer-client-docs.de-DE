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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432233"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="87817-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="87817-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="87817-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87817-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87817-105">Sucht ein lokales Pfad-Gegenstück zum angegebenen Unc-Pfad (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="87817-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87817-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="87817-106">Header file:</span></span>  <br/> |<span data-ttu-id="87817-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="87817-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="87817-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="87817-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="87817-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="87817-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="87817-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="87817-110">Called by:</span></span>  <br/> |<span data-ttu-id="87817-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="87817-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="87817-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87817-112">Parameters</span></span>

 <span data-ttu-id="87817-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="87817-113">_szUNC_</span></span>
  
> <span data-ttu-id="87817-114">[in] Ein Pfad im Format \\ [ _server_] \[ _share_] \[ _path_] einer Datei oder eines Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="87817-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="87817-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="87817-115">_szLocal_</span></span>
  
> <span data-ttu-id="87817-116">[out] Ein Pfad im Format [ _drive:_] path ] derselben Datei oder desselben Verzeichnisses \[ wie für den _szUNC-Parameter._</span><span class="sxs-lookup"><span data-stu-id="87817-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="87817-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="87817-117">_cchLocal_</span></span>
  
> <span data-ttu-id="87817-118">[in] Größe des Puffers für die Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="87817-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87817-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87817-119">Return value</span></span>

<span data-ttu-id="87817-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="87817-120">S_OK</span></span>
  
> <span data-ttu-id="87817-121">Ein lokaler Pfad wurde erfolgreich lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="87817-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="87817-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="87817-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="87817-123">_szLocal war_ nicht groß genug, um das Ergebnis zu halten.</span><span class="sxs-lookup"><span data-stu-id="87817-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="87817-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="87817-124">S_FALSE</span></span>
  
> <span data-ttu-id="87817-125">Die UNC-Zeichenfolge war bereits ein lokaler Pfad.</span><span class="sxs-lookup"><span data-stu-id="87817-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="87817-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="87817-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="87817-127">Ein lokaler Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="87817-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87817-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87817-128">See also</span></span>



[<span data-ttu-id="87817-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="87817-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

