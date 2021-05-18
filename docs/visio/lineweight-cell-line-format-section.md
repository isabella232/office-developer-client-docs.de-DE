---
title: Zelle "LineWeight" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412247"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="20e17-104">Zelle "LineWeight" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="20e17-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="20e17-p102">Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.</span><span class="sxs-lookup"><span data-stu-id="20e17-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20e17-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20e17-107">Remarks</span></span>

<span data-ttu-id="20e17-108">Sie können den Wert von LineWeight auch im  Dialogfeld Linie festlegen (klicken Sie auf der Registerkarte Start in der **Gruppe Shape** auf **Linie,** zeigen Sie auf **Gewichtung,** und klicken Sie dann auf **Weitere Linien**). </span><span class="sxs-lookup"><span data-stu-id="20e17-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="20e17-109">Wenn die Maßeinheit nicht eingegeben wird, wird die Maßeinheit für text verwendet, die  im Dialogfeld **Visio Optionen** angegeben ist (klicken Sie auf die Registerkarte Datei, und klicken Sie dann auf **Optionen**).</span><span class="sxs-lookup"><span data-stu-id="20e17-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="20e17-110">Die Linienbreite ist unabhängig vom Zeichnungsmaßstab.</span><span class="sxs-lookup"><span data-stu-id="20e17-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="20e17-111">Wenn die Zeichnung maßstäblich ist, bleibt die Linienbreite unverändert.</span><span class="sxs-lookup"><span data-stu-id="20e17-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="20e17-112">Verwenden Sie zum Erhalten eines Verweises auf die Zelle LineWeight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="20e17-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20e17-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="20e17-113">Cell name:</span></span>  <br/> | <span data-ttu-id="20e17-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="20e17-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="20e17-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineWeight-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="20e17-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20e17-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="20e17-116">Section index:</span></span>  <br/> |<span data-ttu-id="20e17-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20e17-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20e17-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="20e17-118">Row index:</span></span>  <br/> |<span data-ttu-id="20e17-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="20e17-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="20e17-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="20e17-120">Cell index:</span></span>  <br/> |<span data-ttu-id="20e17-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="20e17-121">**visLineWeight**</span></span> <br/> |
   

