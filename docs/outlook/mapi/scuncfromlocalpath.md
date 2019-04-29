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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414536"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="a87d7-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="a87d7-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="a87d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a87d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a87d7-105">Sucht einen UNC-Pfad Gegenstück (Universal Naming Convention) für den angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="a87d7-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a87d7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a87d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="a87d7-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a87d7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a87d7-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a87d7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a87d7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a87d7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a87d7-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a87d7-110">Called by:</span></span>  <br/> |<span data-ttu-id="a87d7-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a87d7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="a87d7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a87d7-112">Parameters</span></span>

 <span data-ttu-id="a87d7-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="a87d7-113">_szLocal_</span></span>
  
> <span data-ttu-id="a87d7-114">in Ein Pfad im Format [ _Drive:_]\[ _path_] einer Datei oder eines Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="a87d7-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="a87d7-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="a87d7-115">_szUNC_</span></span>
  
> <span data-ttu-id="a87d7-116">Out Ein Pfad im \\Format [ _Server_]\[ _Freigabe_\[ _Pfad_] derselben Datei oder desselben Verzeichnisses wie für den _szLocal_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="a87d7-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="a87d7-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="a87d7-117">_cchUNC_</span></span>
  
> <span data-ttu-id="a87d7-118">in Die Größe des Puffers für die Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a87d7-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a87d7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a87d7-119">Return value</span></span>

<span data-ttu-id="a87d7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a87d7-120">S_OK</span></span>
  
> <span data-ttu-id="a87d7-121">Der UNC-Pfad Gegenstück wurde erfolgreich gefunden.</span><span class="sxs-lookup"><span data-stu-id="a87d7-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="a87d7-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a87d7-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="a87d7-123">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a87d7-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="a87d7-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="a87d7-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="a87d7-125">_szUNC_ war nicht groß genug, um das Ergebnis zu halten.</span><span class="sxs-lookup"><span data-stu-id="a87d7-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="a87d7-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a87d7-126">S_FALSE</span></span>
  
> <span data-ttu-id="a87d7-127">Der lokale Pfad war bereits eine UNC-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a87d7-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a87d7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a87d7-128">See also</span></span>



[<span data-ttu-id="a87d7-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="a87d7-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

