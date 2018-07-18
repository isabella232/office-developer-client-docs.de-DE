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
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="02b0f-103">EndArrow Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="02b0f-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="02b0f-104">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="02b0f-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="02b0f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="02b0f-105">**Value**</span></span>|<span data-ttu-id="02b0f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02b0f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02b0f-107">0</span><span class="sxs-lookup"><span data-stu-id="02b0f-107">0</span></span>  <br/> |<span data-ttu-id="02b0f-108">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="02b0f-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="02b0f-109">1 – 45</span><span class="sxs-lookup"><span data-stu-id="02b0f-109">1 - 45</span></span>  <br/> |<span data-ttu-id="02b0f-110">Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="02b0f-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02b0f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02b0f-111">Remarks</span></span>

<span data-ttu-id="02b0f-112">Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).</span><span class="sxs-lookup"><span data-stu-id="02b0f-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="02b0f-113">Die Größe der Pfeilspitze wird in die Zelle EndArrowSize festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02b0f-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="02b0f-114">Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben.</span><span class="sxs-lookup"><span data-stu-id="02b0f-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="02b0f-115">Wenn Sie einen Verweis auf die Zelle EndArrow aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02b0f-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02b0f-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="02b0f-116">Cell name:</span></span>  <br/> |<span data-ttu-id="02b0f-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="02b0f-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="02b0f-118">Wenn Sie einen Verweis auf die Zelle EndArrow aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="02b0f-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02b0f-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="02b0f-119">Section index:</span></span>  <br/> |<span data-ttu-id="02b0f-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02b0f-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="02b0f-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="02b0f-121">Row index:</span></span>  <br/> |<span data-ttu-id="02b0f-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="02b0f-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="02b0f-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="02b0f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="02b0f-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="02b0f-124">**visLineEndArrow**</span></span> <br/> |
   

