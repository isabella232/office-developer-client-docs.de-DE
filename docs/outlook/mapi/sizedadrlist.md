---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795530"
---
# <a name="sizedadrlist"></a><span data-ttu-id="006dc-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="006dc-103">SizedADRLIST</span></span>

<span data-ttu-id="006dc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="006dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="006dc-105">Definiert eine [ADRLIST](adrlist.md) -Struktur mit dem angegebenen Namen, der eine angegebene Anzahl von [ADRENTRY](adrentry.md) Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="006dc-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="006dc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="006dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="006dc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="006dc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="006dc-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="006dc-108">Related structure:</span></span>  <br/> |<span data-ttu-id="006dc-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="006dc-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="006dc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="006dc-110">Parameters</span></span>

<span data-ttu-id="006dc-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="006dc-111">__centries_</span></span>
  
> <span data-ttu-id="006dc-112">Anzahl der **ADRENTRY** Strukturen, die in der neuen **ADRLIST** -Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="006dc-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="006dc-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="006dc-113">__name_</span></span>
  
> <span data-ttu-id="006dc-114">Der Name für die neue **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="006dc-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="006dc-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="006dc-115">Remarks</span></span>

<span data-ttu-id="006dc-116">Das Makro **SizedADRLIST** können Sie eine Empfängerliste definieren, die explizite Grenzen hat, wenn Array Länge Anforderungen bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="006dc-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="006dc-117">Der folgende Code zeigt, wie das Ergebnis des **SizedADRLIST** Makros in einer **ADRLIST** Struktur Zeiger umgewandelt wird:</span><span class="sxs-lookup"><span data-stu-id="006dc-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="006dc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="006dc-118">See also</span></span>

- [<span data-ttu-id="006dc-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="006dc-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="006dc-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="006dc-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="006dc-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="006dc-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

