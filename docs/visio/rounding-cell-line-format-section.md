---
title: Zelle "Rounding" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797886"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="f7d2d-105">Rounding Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="f7d2d-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="f7d2d-p102">Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).</span><span class="sxs-lookup"><span data-stu-id="f7d2d-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7d2d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7d2d-109">Remarks</span></span>

<span data-ttu-id="f7d2d-110">Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Weight**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="f7d2d-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="f7d2d-111">Wenn Sie einen Verweis auf die Zelle Rounding aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f7d2d-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7d2d-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f7d2d-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f7d2d-113">Rounding</span><span class="sxs-lookup"><span data-stu-id="f7d2d-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="f7d2d-114">Wenn Sie einen Verweis auf die Zelle Rounding aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f7d2d-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7d2d-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f7d2d-115">Section index:</span></span>  <br/> |<span data-ttu-id="f7d2d-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f7d2d-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f7d2d-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f7d2d-117">Row index:</span></span>  <br/> |<span data-ttu-id="f7d2d-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="f7d2d-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="f7d2d-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f7d2d-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f7d2d-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="f7d2d-120">**visLineRounding**</span></span> <br/> |
   

