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
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434683"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="dbcc8-103">Zelle "EndArrow" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="dbcc8-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="dbcc8-104">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="dbcc8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dbcc8-105">**Value**</span></span>|<span data-ttu-id="dbcc8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbcc8-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbcc8-107">0</span><span class="sxs-lookup"><span data-stu-id="dbcc8-107">0</span></span>  <br/> |<span data-ttu-id="dbcc8-108">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="dbcc8-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="dbcc8-109">1 - 45</span><span class="sxs-lookup"><span data-stu-id="dbcc8-109">1 - 45</span></span>  <br/> |<span data-ttu-id="dbcc8-110">Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbcc8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dbcc8-111">Remarks</span></span>

<span data-ttu-id="dbcc8-112">Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).</span><span class="sxs-lookup"><span data-stu-id="dbcc8-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="dbcc8-113">Die Größe der Pfeilspitze wird in der Zelle EndArrowSize festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="dbcc8-114">Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="dbcc8-115">Verwenden Sie zum Erhalten eines Verweises auf die Zelle EndArrow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="dbcc8-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbcc8-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dbcc8-116">Cell name:</span></span>  <br/> |<span data-ttu-id="dbcc8-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="dbcc8-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="dbcc8-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EndArrow-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="dbcc8-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbcc8-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dbcc8-119">Section index:</span></span>  <br/> |<span data-ttu-id="dbcc8-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dbcc8-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dbcc8-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dbcc8-121">Row index:</span></span>  <br/> |<span data-ttu-id="dbcc8-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="dbcc8-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="dbcc8-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dbcc8-123">Cell index:</span></span>  <br/> |<span data-ttu-id="dbcc8-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="dbcc8-124">**visLineEndArrow**</span></span> <br/> |
   

