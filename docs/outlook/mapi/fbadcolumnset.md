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
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575098"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="36472-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="36472-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="36472-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36472-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36472-105">Legen Sie die Gültigkeit einer Tabellenspalte für Tests verwenden, indem Sie einem Dienstanbieter in einem nachfolgenden Aufruf der [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="36472-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36472-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="36472-106">Header file:</span></span>  <br/> |<span data-ttu-id="36472-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="36472-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="36472-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="36472-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36472-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36472-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36472-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="36472-110">Called by:</span></span>  <br/> |<span data-ttu-id="36472-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="36472-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="36472-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="36472-112">Parameters</span></span>

 <span data-ttu-id="36472-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="36472-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="36472-114">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags definieren die Tabellenspalten überprüfen enthält.</span><span class="sxs-lookup"><span data-stu-id="36472-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36472-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="36472-115">Return value</span></span>

<span data-ttu-id="36472-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="36472-116">TRUE</span></span> 
  
> <span data-ttu-id="36472-117">Der angegebene Spalte ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="36472-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="36472-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="36472-118">FALSE</span></span> 
  
> <span data-ttu-id="36472-119">Der angegebene Spalte ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="36472-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36472-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="36472-120">Remarks</span></span>

<span data-ttu-id="36472-121">Die **FBadColumnSet** -Funktion wird vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als ungültig behandelt.</span><span class="sxs-lookup"><span data-stu-id="36472-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

