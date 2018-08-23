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
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592332"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="58e91-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="58e91-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="58e91-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58e91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58e91-105">Ruft die Adresse der Verteilungsfunktion Standard MAPI-Speicher.</span><span class="sxs-lookup"><span data-stu-id="58e91-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58e91-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="58e91-106">Header file:</span></span>  <br/> |<span data-ttu-id="58e91-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="58e91-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="58e91-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="58e91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="58e91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="58e91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="58e91-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="58e91-110">Called by:</span></span>  <br/> |<span data-ttu-id="58e91-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="58e91-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="58e91-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="58e91-112">Parameters</span></span>

<span data-ttu-id="58e91-113">None.</span><span class="sxs-lookup"><span data-stu-id="58e91-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="58e91-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58e91-114">Return value</span></span>

<span data-ttu-id="58e91-115">Die **MAPIGetDefaultMalloc** -Funktion gibt einen Zeiger auf die Standardfunktion MAPI Memory Allocation.</span><span class="sxs-lookup"><span data-stu-id="58e91-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

