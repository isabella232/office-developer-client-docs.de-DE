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
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793113"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="f1cbb-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="f1cbb-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="f1cbb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1cbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1cbb-105">Ruft die Adresse der Verteilungsfunktion Standard MAPI-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f1cbb-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1cbb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f1cbb-106">Header file:</span></span>  <br/> |<span data-ttu-id="f1cbb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f1cbb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f1cbb-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f1cbb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f1cbb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f1cbb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f1cbb-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f1cbb-110">Called by:</span></span>  <br/> |<span data-ttu-id="f1cbb-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f1cbb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="f1cbb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1cbb-112">Parameters</span></span>

<span data-ttu-id="f1cbb-113">None.</span><span class="sxs-lookup"><span data-stu-id="f1cbb-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="f1cbb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1cbb-114">Return value</span></span>

<span data-ttu-id="f1cbb-115">Die **MAPIGetDefaultMalloc** -Funktion gibt einen Zeiger auf die Standardfunktion MAPI Memory Allocation.</span><span class="sxs-lookup"><span data-stu-id="f1cbb-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

