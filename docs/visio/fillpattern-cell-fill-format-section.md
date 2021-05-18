---
title: Zelle "FillPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422929"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="159fa-104">Zelle "FillPattern" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="159fa-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="159fa-p102">Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.</span><span class="sxs-lookup"><span data-stu-id="159fa-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="159fa-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="159fa-107">**Value**</span></span>|<span data-ttu-id="159fa-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="159fa-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="159fa-109">0</span><span class="sxs-lookup"><span data-stu-id="159fa-109">0</span></span>  <br/> |<span data-ttu-id="159fa-110">Keine (transparente Füllung).</span><span class="sxs-lookup"><span data-stu-id="159fa-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="159fa-111">1</span><span class="sxs-lookup"><span data-stu-id="159fa-111">1</span></span>  <br/> |<span data-ttu-id="159fa-112">Einfarbige Vordergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="159fa-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="159fa-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="159fa-113">2 - 40</span></span>  <br/> |<span data-ttu-id="159fa-114">Verschiedene Füllmuster, die den indizierten Einträgen im Dialogfeld **Füllbereich** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="159fa-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="159fa-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="159fa-115">Remarks</span></span>

<span data-ttu-id="159fa-116">Sie können diesen Wert auch über das Dialogfeld **Füllbereich** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).</span><span class="sxs-lookup"><span data-stu-id="159fa-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="159fa-117">Um einen Verweis auf die FillPattern-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="159fa-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="159fa-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="159fa-118">Cell name:</span></span>  <br/> |<span data-ttu-id="159fa-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="159fa-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="159fa-120">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die FillPattern-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="159fa-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="159fa-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="159fa-121">Section index:</span></span>  <br/> |<span data-ttu-id="159fa-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="159fa-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="159fa-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="159fa-123">Row index:</span></span>  <br/> |<span data-ttu-id="159fa-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="159fa-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="159fa-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="159fa-125">Cell index:</span></span>  <br/> |<span data-ttu-id="159fa-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="159fa-126">**visFillPattern**</span></span> <br/> |
   

