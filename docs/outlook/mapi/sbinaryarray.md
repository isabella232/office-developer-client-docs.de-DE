---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795425"
---
# <a name="sbinaryarray"></a><span data-ttu-id="2cf27-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="2cf27-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="2cf27-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cf27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cf27-105">Enthält ein Array von binären Werten.</span><span class="sxs-lookup"><span data-stu-id="2cf27-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cf27-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2cf27-106">Header file:</span></span>  <br/> |<span data-ttu-id="2cf27-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cf27-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="2cf27-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="2cf27-108">Members</span></span>

 <span data-ttu-id="2cf27-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2cf27-109">**cValues**</span></span>
  
> <span data-ttu-id="2cf27-110">Anzahl der Werte im Array auf den Member **Lpbin** zeigt.</span><span class="sxs-lookup"><span data-stu-id="2cf27-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="2cf27-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="2cf27-111">**lpbin**</span></span>
  
> <span data-ttu-id="2cf27-112">Zeiger auf ein Array von [SBinary](sbinary.md) -Strukturen, die binäre Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="2cf27-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2cf27-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cf27-113">Remarks</span></span>

<span data-ttu-id="2cf27-114">Die Struktur **SBinaryArray** wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2cf27-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="2cf27-115">Weitere Informationen zu PT_MV_BINARY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2cf27-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cf27-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cf27-116">See also</span></span>



[<span data-ttu-id="2cf27-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="2cf27-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="2cf27-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2cf27-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2cf27-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2cf27-119">MAPI Structures</span></span>](mapi-structures.md)

