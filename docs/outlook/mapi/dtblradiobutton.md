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
ms.openlocfilehash: 493176029be3e7b154188aa164a95a8bc9c0e7d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569743"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="3a996-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="3a996-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="3a996-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a996-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a996-105">Beschreibt ein Optionsfeld, die an eine Gruppe von Optionsfeldern werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a996-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="3a996-106">Die Gruppe von Optionsfeldern wird in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a996-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a996-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3a996-107">Header file:</span></span>  <br/> |<span data-ttu-id="3a996-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a996-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="3a996-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="3a996-109">Members</span></span>

 <span data-ttu-id="3a996-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="3a996-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="3a996-111">Die Position im Speicher der Zeichen Zeichenfolge Bezeichnung für das Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="3a996-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="3a996-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3a996-112">**ulFlags**</span></span>
  
> <span data-ttu-id="3a996-113">Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabel** Member.</span><span class="sxs-lookup"><span data-stu-id="3a996-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="3a996-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3a996-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="3a996-115">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a996-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3a996-116">Die Beschriftung wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="3a996-116">The label is in Unicode format.</span></span> <span data-ttu-id="3a996-117">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="3a996-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="3a996-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="3a996-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="3a996-119">Anzahl der Schaltflächen in der Gruppe von Optionsfeldern.</span><span class="sxs-lookup"><span data-stu-id="3a996-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="3a996-120">Die **DTBLRADIOBUTTON** Strukturen für die anderen Schaltflächen in der Gruppe müssen in aufeinander folgenden Zeilen der Tabelle anzeigen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3a996-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="3a996-121">Jeder dieser Zeilen sollte den gleichen Wert für das **UlcButtons** -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a996-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="3a996-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="3a996-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="3a996-123">Eigenschaftentag für eine Eigenschaft vom Typ PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="3a996-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="3a996-124">Die ursprüngliche Auswahl in die Gruppe von Optionsfeldern basiert auf den ursprünglichen Wert dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3a996-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="3a996-125">Jede Schaltfläche in der Gruppe benötigen **UlPropTag** auf dieselbe Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a996-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="3a996-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="3a996-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="3a996-127">Eindeutige Zahl, die die ausgewählte Schaltfläche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3a996-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a996-128">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3a996-128">Remarks</span></span>

<span data-ttu-id="3a996-129">Eine Struktur **DTBLRADIOBUTTON** beschreibt ein Optionsfeld ein Button-Steuerelement, das eine Gruppe von Schaltflächen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3a996-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="3a996-130">Es kann nur eine Schaltfläche in der Gruppe überprüft werden soll; Festlegen einer Schaltfläche bewirkt, dass die anderen Schaltflächen in der Gruppe nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a996-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="3a996-131">Der Wert der Schaltfläche wird die Anzahl der Optionsfelder in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3a996-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="3a996-132">Die Strukturen für die anderen Optionsfelder in der Gruppe müssen in folgenden Zeilen in der Tabelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a996-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="3a996-133">Jedes dieser Strukturen sollte den gleichen Wert für die Anzahl der Schaltfläche aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3a996-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="3a996-134">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3a996-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3a996-135">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="3a996-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a996-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a996-136">See also</span></span>



[<span data-ttu-id="3a996-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="3a996-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="3a996-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3a996-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="3a996-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="3a996-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="3a996-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3a996-140">MAPI Structures</span></span>](mapi-structures.md)

