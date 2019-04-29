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
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="cdfec-103">Zelle "EndArrow" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="cdfec-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="cdfec-104">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="cdfec-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="cdfec-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cdfec-105">**Value**</span></span>|<span data-ttu-id="cdfec-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdfec-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdfec-107">0</span><span class="sxs-lookup"><span data-stu-id="cdfec-107">0</span></span>  <br/> |<span data-ttu-id="cdfec-108">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="cdfec-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="cdfec-109">1 - 45</span><span class="sxs-lookup"><span data-stu-id="cdfec-109">1 - 45</span></span>  <br/> |<span data-ttu-id="cdfec-110">Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cdfec-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdfec-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdfec-111">Remarks</span></span>

<span data-ttu-id="cdfec-112">Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).</span><span class="sxs-lookup"><span data-stu-id="cdfec-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="cdfec-113">Die Größe der Pfeilspitze wird in der Zelle Zelle EndArrowSize festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdfec-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="cdfec-114">Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben.</span><span class="sxs-lookup"><span data-stu-id="cdfec-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="cdfec-115">Wenn Sie einen Verweis auf die Zelle Zelle EndArrow aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cdfec-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cdfec-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cdfec-116">Cell name:</span></span>  <br/> |<span data-ttu-id="cdfec-117">Zelle EndArrow</span><span class="sxs-lookup"><span data-stu-id="cdfec-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="cdfec-118">Wenn Sie einen Verweis auf die Zelle Zelle EndArrow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="cdfec-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cdfec-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cdfec-119">Section index:</span></span>  <br/> |<span data-ttu-id="cdfec-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cdfec-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cdfec-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cdfec-121">Row index:</span></span>  <br/> |<span data-ttu-id="cdfec-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="cdfec-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="cdfec-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="cdfec-123">Cell index:</span></span>  <br/> |<span data-ttu-id="cdfec-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="cdfec-124">**visLineEndArrow**</span></span> <br/> |
   

