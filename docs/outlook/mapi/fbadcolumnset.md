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
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434718"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="0d9f8-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="0d9f8-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="0d9f8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d9f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d9f8-105">Testet die Gültigkeit einer Tabellenspalte, die von einem Dienstanbieter in einem nachfolgenden Aufruf der [IMAPITable::SetColumns-Methode verwendet](imapitable-setcolumns.md) wird.</span><span class="sxs-lookup"><span data-stu-id="0d9f8-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d9f8-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="0d9f8-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d9f8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0d9f8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0d9f8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0d9f8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d9f8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d9f8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d9f8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0d9f8-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d9f8-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0d9f8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="0d9f8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d9f8-112">Parameters</span></span>

 <span data-ttu-id="0d9f8-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="0d9f8-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="0d9f8-114">[in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die zu überprüfenden Tabellenspalten definieren.</span><span class="sxs-lookup"><span data-stu-id="0d9f8-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d9f8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d9f8-115">Return value</span></span>

<span data-ttu-id="0d9f8-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="0d9f8-116">TRUE</span></span> 
  
> <span data-ttu-id="0d9f8-117">Der angegebene Spaltensatz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0d9f8-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="0d9f8-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="0d9f8-118">FALSE</span></span> 
  
> <span data-ttu-id="0d9f8-119">Der angegebene Spaltensatz ist gültig.</span><span class="sxs-lookup"><span data-stu-id="0d9f8-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d9f8-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d9f8-120">Remarks</span></span>

<span data-ttu-id="0d9f8-121">Die **FBadColumnSet-Funktion** behandelt Spalten vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als gültig.</span><span class="sxs-lookup"><span data-stu-id="0d9f8-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

