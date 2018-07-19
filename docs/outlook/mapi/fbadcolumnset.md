---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791666"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="c4640-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="c4640-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="c4640-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4640-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4640-105">Legen Sie die Gültigkeit einer Tabellenspalte für Tests verwenden, indem Sie einem Dienstanbieter in einem nachfolgenden Aufruf der [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c4640-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4640-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c4640-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4640-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c4640-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c4640-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c4640-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4640-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4640-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4640-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c4640-110">Called by:</span></span>  <br/> |<span data-ttu-id="c4640-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c4640-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="c4640-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4640-112">Parameters</span></span>

 <span data-ttu-id="c4640-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="c4640-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="c4640-114">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags definieren die Tabellenspalten überprüfen enthält.</span><span class="sxs-lookup"><span data-stu-id="c4640-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c4640-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4640-115">Return value</span></span>

<span data-ttu-id="c4640-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4640-116">TRUE</span></span> 
  
> <span data-ttu-id="c4640-117">Der angegebene Spalte ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c4640-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="c4640-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4640-118">FALSE</span></span> 
  
> <span data-ttu-id="c4640-119">Der angegebene Spalte ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c4640-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4640-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4640-120">Remarks</span></span>

<span data-ttu-id="c4640-121">Die **FBadColumnSet** -Funktion wird vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als ungültig behandelt.</span><span class="sxs-lookup"><span data-stu-id="c4640-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

