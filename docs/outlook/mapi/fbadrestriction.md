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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d729e2a12ee19ee3aa4ded71263697eb739f154
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566306"
---
# <a name="fbadrestriction"></a><span data-ttu-id="9ca4a-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="9ca4a-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="9ca4a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ca4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ca4a-105">Überprüft eine Einschränkung verwendet, um einer Tabellenansicht einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ca4a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9ca4a-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ca4a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9ca4a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9ca4a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9ca4a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9ca4a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9ca4a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9ca4a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9ca4a-110">Called by:</span></span>  <br/> |<span data-ttu-id="9ca4a-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9ca4a-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="9ca4a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ca4a-112">Parameters</span></span>

 <span data-ttu-id="9ca4a-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="9ca4a-113">_lpres_</span></span>
  
> <span data-ttu-id="9ca4a-114">[in] Eine [SRestriction](srestriction.md) -Struktur definieren die Einschränkung überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ca4a-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9ca4a-115">Return value</span></span>

<span data-ttu-id="9ca4a-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="9ca4a-116">TRUE</span></span> 
  
> <span data-ttu-id="9ca4a-117">Die angegebene Einschränkung oder eine oder mehrere der seine Subrestrictions ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="9ca4a-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="9ca4a-118">FALSE</span></span> 
  
> <span data-ttu-id="9ca4a-119">Die angegebene Beschränkung und alle seine Subrestrictions sind gültig.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ca4a-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9ca4a-120">Remarks</span></span>

<span data-ttu-id="9ca4a-121">Nach der Überprüfung einer Einschränkung, kann sie in der Tabelle auf bestimmte Zeilen, an die [IMAPITable](imapitable-findrow.md) -Methode, um eine Tabellenzeile zu suchen und die Methoden des der [IMAPIContainer](imapicontainerimapiprop.md) einschränken Aufrufen an die [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode übergeben werden Schnittstelle für eine Beschränkung für ein Container-Objekt ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

