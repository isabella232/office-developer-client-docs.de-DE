---
title: Zelle "ShdwPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Definiert das Füllmuster für den Schatten eines Shapes.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427612"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="8a29a-103">Zelle "ShdwPattern" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="8a29a-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="8a29a-104">Definiert das Füllmuster für den Schatten eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="8a29a-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="8a29a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8a29a-105">**Value**</span></span>|<span data-ttu-id="8a29a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a29a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a29a-107">0</span><span class="sxs-lookup"><span data-stu-id="8a29a-107">0</span></span>  <br/> |<span data-ttu-id="8a29a-108">Keins (transparente Füllung).</span><span class="sxs-lookup"><span data-stu-id="8a29a-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="8a29a-109">1</span><span class="sxs-lookup"><span data-stu-id="8a29a-109">1</span></span>  <br/> |<span data-ttu-id="8a29a-110">Einfarbige Vordergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="8a29a-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="8a29a-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="8a29a-111">2 - 40</span></span>  <br/> |<span data-ttu-id="8a29a-112">Verschiedene Füllmuster</span><span class="sxs-lookup"><span data-stu-id="8a29a-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a29a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a29a-113">Remarks</span></span>

<span data-ttu-id="8a29a-p101">Wenn Sie das Füllmuster festlegen möchten, geben Sie eine Zahl von 0 bis 40 ein. Diese Zahl ist ein Index für eine Mustersammlung. Sie können sich die Füllmustersammlung auch im Dialogfeld **Füllbereich** ansehen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).</span><span class="sxs-lookup"><span data-stu-id="8a29a-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="8a29a-116">Verwenden Sie zum Rufen eines Verweises auf die ShdwPattern-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="8a29a-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a29a-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8a29a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="8a29a-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="8a29a-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="8a29a-119">Um einen Verweis auf die ShdwPattern-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8a29a-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a29a-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8a29a-120">Section index:</span></span>  <br/> |<span data-ttu-id="8a29a-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8a29a-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8a29a-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8a29a-122">Row index:</span></span>  <br/> |<span data-ttu-id="8a29a-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8a29a-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="8a29a-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8a29a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8a29a-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="8a29a-125">**visFillShdwPattern**</span></span> <br/> |
   

