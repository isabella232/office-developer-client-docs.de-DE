---
title: Zelle "LinePattern" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416755"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="04487-104">Zelle "LinePattern" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="04487-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="04487-p102">Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.</span><span class="sxs-lookup"><span data-stu-id="04487-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="04487-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="04487-107">**Value**</span></span>|<span data-ttu-id="04487-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04487-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04487-109">0</span><span class="sxs-lookup"><span data-stu-id="04487-109">0</span></span>  <br/> |<span data-ttu-id="04487-110">Kein Linienmuster</span><span class="sxs-lookup"><span data-stu-id="04487-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="04487-111">1</span><span class="sxs-lookup"><span data-stu-id="04487-111">1</span></span>  <br/> |<span data-ttu-id="04487-112">Einfarbig</span><span class="sxs-lookup"><span data-stu-id="04487-112">Solid</span></span>  <br/> |
|<span data-ttu-id="04487-113">2 - 23</span><span class="sxs-lookup"><span data-stu-id="04487-113">2 - 23</span></span>  <br/> |<span data-ttu-id="04487-114">Verschiedene Linienmuster</span><span class="sxs-lookup"><span data-stu-id="04487-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04487-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04487-115">Remarks</span></span>

<span data-ttu-id="04487-116">Sie können sich die Linienmustersammlung auch im Dialogfeld **Linie** ansehen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Strichlinien**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="04487-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="04487-117">Um ein benutzerdefiniertes Linienmuster anzugeben, verwenden Sie die Funktion VERWENDUNG in dieser Zelle.</span><span class="sxs-lookup"><span data-stu-id="04487-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="04487-118">Verwenden Sie zum Erhalten eines Verweises auf die Zelle LinePattern anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="04487-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04487-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="04487-119">Cell name:</span></span>  <br/> |<span data-ttu-id="04487-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="04487-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="04487-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LinePattern-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="04487-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04487-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="04487-122">Section index:</span></span>  <br/> |<span data-ttu-id="04487-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04487-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="04487-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="04487-124">Row index:</span></span>  <br/> |<span data-ttu-id="04487-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="04487-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="04487-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="04487-126">Cell index:</span></span>  <br/> |<span data-ttu-id="04487-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="04487-127">**visLinePattern**</span></span> <br/> |
   

