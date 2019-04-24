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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345776"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="fe95f-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="fe95f-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="fe95f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe95f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe95f-105">Ruft die Adresse der standardmäßigen MAPI-Speicher Zuordnungsfunktion ab.</span><span class="sxs-lookup"><span data-stu-id="fe95f-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe95f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fe95f-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe95f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="fe95f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fe95f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fe95f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fe95f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fe95f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fe95f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fe95f-110">Called by:</span></span>  <br/> |<span data-ttu-id="fe95f-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fe95f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="fe95f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe95f-112">Parameters</span></span>

<span data-ttu-id="fe95f-113">None.</span><span class="sxs-lookup"><span data-stu-id="fe95f-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="fe95f-114">Return value</span><span class="sxs-lookup"><span data-stu-id="fe95f-114">Return value</span></span>

<span data-ttu-id="fe95f-115">Die **MAPIGetDefaultMalloc** -Funktion gibt einen Zeiger auf die standardmäßige MAPI-Speicher Zuordnungsfunktion zurück.</span><span class="sxs-lookup"><span data-stu-id="fe95f-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

