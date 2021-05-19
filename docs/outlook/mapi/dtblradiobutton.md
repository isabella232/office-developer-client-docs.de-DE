---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434599"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="aa799-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="aa799-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="aa799-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa799-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa799-105">Beschreibt ein Optionsfeld, das Teil einer Optionsfeldgruppe sein wird.</span><span class="sxs-lookup"><span data-stu-id="aa799-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="aa799-106">Die Optionsfeldgruppe wird in einem Dialogfeld verwendet, das aus einer Anzeigetabelle erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="aa799-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa799-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="aa799-107">Header file:</span></span>  <br/> |<span data-ttu-id="aa799-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa799-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a><span data-ttu-id="aa799-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="aa799-109">Members</span></span>

 <span data-ttu-id="aa799-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="aa799-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="aa799-111">Position im Speicher der Zeichenzeichenfolgenbeschriftung für das Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="aa799-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="aa799-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="aa799-112">**ulFlags**</span></span>
  
> <span data-ttu-id="aa799-113">Bitmaske von Flags, die verwendet werden, um das Format der Bezeichnung zu bestimmen, auf das das **ulbLpszLabel-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="aa799-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="aa799-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="aa799-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="aa799-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aa799-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aa799-116">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="aa799-116">The label is in Unicode format.</span></span> <span data-ttu-id="aa799-117">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="aa799-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="aa799-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="aa799-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="aa799-119">Anzahl der Schaltflächen in der Optionsfeldgruppe.</span><span class="sxs-lookup"><span data-stu-id="aa799-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="aa799-120">Die **DTBLRADIOBUTTON-Strukturen** für die anderen Schaltflächen in der Gruppe müssen in aufeinander folgenden Zeilen der Anzeigetabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="aa799-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="aa799-121">Jede dieser Zeilen sollte denselben Wert für das **ulcButtons-Element** enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa799-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="aa799-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="aa799-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="aa799-123">Eigenschaftstag für eine Eigenschaft vom Typ PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="aa799-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="aa799-124">Die anfängliche Auswahl in der Optionsfeldgruppe basiert auf dem Anfangswert dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aa799-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="aa799-125">Für jede Schaltfläche in der Gruppe muss **ulPropTag auf** dieselbe Eigenschaft festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="aa799-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="aa799-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="aa799-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="aa799-127">Eindeutige Nummer, die die ausgewählte Schaltfläche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa799-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa799-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa799-128">Remarks</span></span>

<span data-ttu-id="aa799-129">Eine **DTBLRADIOBUTTON-Struktur** beschreibt ein Optionsfeld ein Schaltflächensteuerelement, das einer Gruppe von Schaltflächen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aa799-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="aa799-130">Es kann nur eine Schaltfläche in der Gruppe aktiviert werden. Wenn Sie eine Schaltfläche festlegen, werden die anderen Schaltflächen in der Gruppe nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa799-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="aa799-131">Die Anzahl der Schaltflächen ist die Anzahl der Optionsfelder in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="aa799-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="aa799-132">Die Strukturen für die anderen Optionsfelder in der Gruppe müssen sich in nachfolgenden Zeilen in der Anzeigetabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa799-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="aa799-133">Jede dieser Strukturen sollte denselben Wert für die Anzahl der Schaltflächen haben.</span><span class="sxs-lookup"><span data-stu-id="aa799-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="aa799-134">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="aa799-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="aa799-135">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="aa799-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa799-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa799-136">See also</span></span>



[<span data-ttu-id="aa799-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="aa799-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="aa799-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="aa799-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="aa799-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="aa799-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="aa799-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="aa799-140">MAPI Structures</span></span>](mapi-structures.md)

