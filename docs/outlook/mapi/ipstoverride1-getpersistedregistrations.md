---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575868"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="e08a4-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="e08a4-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="e08a4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e08a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e08a4-105">Ruft die Liste von Einträgen für den persönlichen Ordner (PST) Datei ab.</span><span class="sxs-lookup"><span data-stu-id="e08a4-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="e08a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e08a4-106">Parameters</span></span>

 <span data-ttu-id="e08a4-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="e08a4-107">_ppmval_</span></span>
  
> <span data-ttu-id="e08a4-108">[in] Ein Zeiger auf einen Zeiger auf eine [SPropValue](spropvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e08a4-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="e08a4-109">Der Member UlPropTag diese Struktur ist vom Typ PT_MV_UNICODE, und das MVszW Element wird ein Array mit Null terminierte Unicode-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="e08a4-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="e08a4-110">Diese Zeichenfolgen sind Pfade zu DLLs für die Registrierung beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="e08a4-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e08a4-111">Unterstützung von ANSI PST-Dateien ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e08a4-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="e08a4-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e08a4-112">Return value</span></span>

<span data-ttu-id="e08a4-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e08a4-113">S_OK</span></span> 
  
> <span data-ttu-id="e08a4-114">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e08a4-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e08a4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e08a4-115">See also</span></span>



[<span data-ttu-id="e08a4-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e08a4-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="e08a4-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e08a4-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

