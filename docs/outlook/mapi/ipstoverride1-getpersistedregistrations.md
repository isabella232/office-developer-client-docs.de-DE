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
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415131"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="4f14d-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="4f14d-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="4f14d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f14d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f14d-105">Ruft die Liste der Registrierungen für die persönliche Ordner-Datei (PST) ab.</span><span class="sxs-lookup"><span data-stu-id="4f14d-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="4f14d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f14d-106">Parameters</span></span>

 <span data-ttu-id="4f14d-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="4f14d-107">_ppmval_</span></span>
  
> <span data-ttu-id="4f14d-108">in Ein Zeiger auf einen Zeiger auf eine [SPropValue](spropvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4f14d-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="4f14d-109">Das ulPropTag-Element dieser Struktur hat den Typ PT_MV_UNICODE, und der MVszW-Wert Member ist ein Array von null-terminierten Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="4f14d-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="4f14d-110">Diese Zeichenfolgen sind Pfade zu DLLs, für die die Registrierung beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="4f14d-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4f14d-111">die PST-Unterstützung für ANSI ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f14d-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="4f14d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f14d-112">Return value</span></span>

<span data-ttu-id="4f14d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f14d-113">S_OK</span></span> 
  
> <span data-ttu-id="4f14d-114">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4f14d-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f14d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f14d-115">See also</span></span>



[<span data-ttu-id="4f14d-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f14d-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="4f14d-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f14d-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

