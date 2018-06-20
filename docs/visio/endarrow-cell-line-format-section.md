---
title: Zelle "EndArrow" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796930"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="7583e-103">EndArrow Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="7583e-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="7583e-104">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="7583e-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="7583e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7583e-105">**Value**</span></span>|<span data-ttu-id="7583e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7583e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7583e-107">0</span><span class="sxs-lookup"><span data-stu-id="7583e-107">0</span></span>  <br/> |<span data-ttu-id="7583e-108">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="7583e-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="7583e-109">1 – 45</span><span class="sxs-lookup"><span data-stu-id="7583e-109">1 - 45</span></span>  <br/> |<span data-ttu-id="7583e-110">Pfeilspitzenformatvorlagen, die indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7583e-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7583e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7583e-111">Remarks</span></span>

<span data-ttu-id="7583e-112">Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).</span><span class="sxs-lookup"><span data-stu-id="7583e-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="7583e-113">Die Größe der Pfeilspitze wird in die Zelle EndArrowSize festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7583e-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="7583e-114">Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben.</span><span class="sxs-lookup"><span data-stu-id="7583e-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="7583e-115">Wenn Sie einen Verweis auf die Zelle EndArrow nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7583e-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7583e-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7583e-116">Cell name:</span></span>  <br/> |<span data-ttu-id="7583e-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="7583e-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="7583e-118">Wenn Sie einen Verweis auf die Zelle EndArrow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7583e-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7583e-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7583e-119">Section index:</span></span>  <br/> |<span data-ttu-id="7583e-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7583e-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7583e-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7583e-121">Row index:</span></span>  <br/> |<span data-ttu-id="7583e-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="7583e-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="7583e-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7583e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7583e-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="7583e-124">**visLineEndArrow**</span></span> <br/> |
   

