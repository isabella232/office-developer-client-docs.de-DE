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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339417"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="e792a-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="e792a-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="e792a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e792a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e792a-105">Beschreibt ein Optionsfeld, das Teil einer Optionsfeldgruppe sein wird.</span><span class="sxs-lookup"><span data-stu-id="e792a-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="e792a-106">Die Optionsschaltfläche-Gruppe wird in einem Dialogfeldverwendet, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e792a-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e792a-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e792a-107">Header file:</span></span>  <br/> |<span data-ttu-id="e792a-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e792a-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e792a-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="e792a-109">Members</span></span>

 <span data-ttu-id="e792a-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="e792a-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="e792a-111">Position im Speicher der Zeichenfolgenbezeichnung für das Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="e792a-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="e792a-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e792a-112">**ulFlags**</span></span>
  
> <span data-ttu-id="e792a-113">Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabel** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e792a-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="e792a-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e792a-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="e792a-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e792a-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e792a-116">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e792a-116">The label is in Unicode format.</span></span> <span data-ttu-id="e792a-117">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e792a-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="e792a-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="e792a-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="e792a-119">Anzahl der Schaltflächen in der Optionsfeldgruppe.</span><span class="sxs-lookup"><span data-stu-id="e792a-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="e792a-120">Die **DTBLRADIOBUTTON** -Strukturen für die anderen Schaltflächen in der Gruppe müssen in aufeinanderfolgenden Zeilen der Anzeigetabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="e792a-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="e792a-121">Jede dieser Zeilen sollte den gleichen Wert für das **ulcButtons** -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="e792a-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="e792a-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e792a-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="e792a-123">Property-Tag für eine Eigenschaft vom Typ PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="e792a-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="e792a-124">Die anfängliche Auswahl in der Optionsfeldgruppe basiert auf dem Anfangswert dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e792a-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="e792a-125">Für jede Schaltfläche in der Gruppe muss **ulPropTag** auf dieselbe Eigenschaft festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="e792a-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="e792a-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="e792a-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="e792a-127">Eindeutige Zahl, die die ausgewählte Schaltfläche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e792a-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e792a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e792a-128">Remarks</span></span>

<span data-ttu-id="e792a-129">Eine **DTBLRADIOBUTTON** -Struktur beschreibt ein Optionsfeld-Steuerelement, das einer Gruppe von Schaltflächen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e792a-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="e792a-130">Nur eine Schaltfläche in der Gruppe kann überprüft werden; durch Festlegen einer Schaltfläche werden die anderen Schaltflächen in der Gruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e792a-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="e792a-131">Die Schaltflächen Anzahl ist die Anzahl der Optionsfelder in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e792a-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="e792a-132">Die Strukturen für die anderen Optionsfelder in der Gruppe müssen sich in nachfolgenden Zeilen in der Anzeigetabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="e792a-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="e792a-133">Jede dieser Strukturen sollte den gleichen Wert für die Schaltflächen Anzahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e792a-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="e792a-134">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e792a-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e792a-135">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e792a-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e792a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e792a-136">See also</span></span>



[<span data-ttu-id="e792a-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="e792a-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="e792a-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e792a-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="e792a-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="e792a-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="e792a-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e792a-140">MAPI Structures</span></span>](mapi-structures.md)

