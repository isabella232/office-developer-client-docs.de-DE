---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340964"
---
# <a name="fbadrestriction"></a><span data-ttu-id="24579-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="24579-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="24579-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24579-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24579-105">Überprüft eine Einschränkung, die zum Einschränken einer Tabellenansicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="24579-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24579-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="24579-106">Header file:</span></span>  <br/> |<span data-ttu-id="24579-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="24579-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="24579-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="24579-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="24579-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="24579-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="24579-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="24579-110">Called by:</span></span>  <br/> |<span data-ttu-id="24579-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="24579-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="24579-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="24579-112">Parameters</span></span>

 <span data-ttu-id="24579-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="24579-113">_lpres_</span></span>
  
> <span data-ttu-id="24579-114">in Eine [SRestriction](srestriction.md) -Struktur, die die zu überprüfende Einschränkung definiert.</span><span class="sxs-lookup"><span data-stu-id="24579-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24579-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24579-115">Return value</span></span>

<span data-ttu-id="24579-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="24579-116">TRUE</span></span> 
  
> <span data-ttu-id="24579-117">Die angegebene Einschränkung oder mindestens eine der unter Einschränkungen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="24579-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="24579-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="24579-118">FALSE</span></span> 
  
> <span data-ttu-id="24579-119">Die angegebene Einschränkung und alle zugehörigen unter Einschränkungen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="24579-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24579-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24579-120">Remarks</span></span>

<span data-ttu-id="24579-121">Sobald eine Einschränkung validiert wurde, kann Sie in Aufrufen der [IMAPITable:: Restrict](imapitable-restrict.md) -Methode übergeben werden, um die Tabelle auf bestimmte Zeilen einzuschränken, auf die [IMAPITable:: FindRow](imapitable-findrow.md) -Methode, um eine Tabellenzeile und die Methoden des [IMAPIContainer](imapicontainerimapiprop.md) zu finden. Schnittstelle zum Durchführen einer Einschränkung für ein Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="24579-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

