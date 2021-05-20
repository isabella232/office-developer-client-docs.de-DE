---
title: Zelle "Value" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431904"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="64502-103">Zelle "Value" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="64502-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="64502-104">Enthält den Wert des Shape-Datenelements, der in das Dialogfeld **Shape-Daten definieren** eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="64502-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="64502-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64502-105">Remarks</span></span>

<span data-ttu-id="64502-p101">Die in diese Zelle eingegebenen Formeln werden von den im Dialogfeld **Shape-Daten definieren** eingegebenen Werten überschrieben. Dies gilt auch, wenn Sie die Formel mithilfe der GUARD-Funktion schützen.</span><span class="sxs-lookup"><span data-stu-id="64502-p101">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box. This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="64502-108">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="64502-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="64502-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="64502-109">Cell name:</span></span>  <br/> | <span data-ttu-id="64502-110">Prop.  *Name*  . Wert, wobei Prop.  *Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="64502-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="64502-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="64502-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="64502-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="64502-112">Section index:</span></span>  <br/> |<span data-ttu-id="64502-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="64502-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="64502-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="64502-114">Row index:</span></span>  <br/> |<span data-ttu-id="64502-115">**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="64502-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="64502-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="64502-116">Cell index:</span></span>  <br/> |<span data-ttu-id="64502-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="64502-117">**visCustPropsValue**</span></span> <br/> |
   

