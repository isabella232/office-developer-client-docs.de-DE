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
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797011"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="e113d-104">FillPattern Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="e113d-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="e113d-p102">Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e113d-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="e113d-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e113d-107">**Value**</span></span>|<span data-ttu-id="e113d-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e113d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e113d-109">0</span><span class="sxs-lookup"><span data-stu-id="e113d-109">0</span></span>  <br/> |<span data-ttu-id="e113d-110">Keine (transparente Füllung).</span><span class="sxs-lookup"><span data-stu-id="e113d-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="e113d-111">1</span><span class="sxs-lookup"><span data-stu-id="e113d-111">1</span></span>  <br/> |<span data-ttu-id="e113d-112">Einfarbige Vordergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="e113d-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="e113d-113">2 – 40</span><span class="sxs-lookup"><span data-stu-id="e113d-113">2 - 40</span></span>  <br/> |<span data-ttu-id="e113d-114">Verschiedene Füllmuster, die den indizierten Einträgen im Dialogfeld **Füllbereich** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e113d-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e113d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e113d-115">Remarks</span></span>

<span data-ttu-id="e113d-116">Sie können diesen Wert auch über das Dialogfeld **Füllbereich** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).</span><span class="sxs-lookup"><span data-stu-id="e113d-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="e113d-117">Wenn Sie einen Verweis auf die Zelle FillPattern aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e113d-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e113d-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e113d-118">Cell name:</span></span>  <br/> |<span data-ttu-id="e113d-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="e113d-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="e113d-120">Wenn Sie einen Verweis auf die Zelle FillPattern aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e113d-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e113d-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e113d-121">Section index:</span></span>  <br/> |<span data-ttu-id="e113d-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e113d-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e113d-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e113d-123">Row index:</span></span>  <br/> |<span data-ttu-id="e113d-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e113d-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="e113d-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e113d-125">Cell index:</span></span>  <br/> |<span data-ttu-id="e113d-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="e113d-126">**visFillPattern**</span></span> <br/> |
   

