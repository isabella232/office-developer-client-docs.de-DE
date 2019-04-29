---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438204"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="a440d-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="a440d-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="a440d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a440d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a440d-105">Ruft die Adresse der standardmäßigen MAPI-Speicher Zuordnungsfunktion ab.</span><span class="sxs-lookup"><span data-stu-id="a440d-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a440d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a440d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a440d-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="a440d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a440d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a440d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a440d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a440d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a440d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a440d-110">Called by:</span></span>  <br/> |<span data-ttu-id="a440d-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a440d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="a440d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a440d-112">Parameters</span></span>

<span data-ttu-id="a440d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a440d-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="a440d-114">Return value</span><span class="sxs-lookup"><span data-stu-id="a440d-114">Return value</span></span>

<span data-ttu-id="a440d-115">Die **MAPIGetDefaultMalloc** -Funktion gibt einen Zeiger auf die standardmäßige MAPI-Speicher Zuordnungsfunktion zurück.</span><span class="sxs-lookup"><span data-stu-id="a440d-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

