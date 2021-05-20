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
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="b11ed-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="b11ed-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="b11ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b11ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b11ed-105">Ruft die Adresse der standardmäßigen MAPI-Speicherzuordnungsfunktion ab.</span><span class="sxs-lookup"><span data-stu-id="b11ed-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b11ed-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b11ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="b11ed-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b11ed-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b11ed-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b11ed-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b11ed-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b11ed-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b11ed-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b11ed-110">Called by:</span></span>  <br/> |<span data-ttu-id="b11ed-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b11ed-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="b11ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b11ed-112">Parameters</span></span>

<span data-ttu-id="b11ed-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b11ed-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="b11ed-114">Return value</span><span class="sxs-lookup"><span data-stu-id="b11ed-114">Return value</span></span>

<span data-ttu-id="b11ed-115">Die **MAPIGetDefaultMalloc-Funktion** gibt einen Zeiger auf die standardmäßige MAPI-Speicherzuordnungsfunktion zurück.</span><span class="sxs-lookup"><span data-stu-id="b11ed-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

