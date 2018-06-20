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
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798078"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="5c18e-103">Zelle "ShdwPattern" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="5c18e-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="5c18e-104">Definiert das Füllmuster für den Schatten eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="5c18e-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="5c18e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5c18e-105">**Value**</span></span>|<span data-ttu-id="5c18e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c18e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c18e-107">0</span><span class="sxs-lookup"><span data-stu-id="5c18e-107">0</span></span>  <br/> |<span data-ttu-id="5c18e-108">Keins (transparente Füllung).</span><span class="sxs-lookup"><span data-stu-id="5c18e-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="5c18e-109">1</span><span class="sxs-lookup"><span data-stu-id="5c18e-109">1</span></span>  <br/> |<span data-ttu-id="5c18e-110">Einfarbige Vordergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="5c18e-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="5c18e-111">2 – 40</span><span class="sxs-lookup"><span data-stu-id="5c18e-111">2 - 40</span></span>  <br/> |<span data-ttu-id="5c18e-112">Verschiedene Füllmuster</span><span class="sxs-lookup"><span data-stu-id="5c18e-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c18e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c18e-113">Remarks</span></span>

<span data-ttu-id="5c18e-114">Um das Füllmuster festgelegt, geben Sie eine Zahl von 0 bis 40, einen Index in einer Auflistung von Muster.</span><span class="sxs-lookup"><span data-stu-id="5c18e-114">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns.</span></span> <span data-ttu-id="5c18e-115">Sie können die Auflistung der Füllung Muster im Dialogfeld **Füllbereich** anzeigen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Füllbereich**, und klicken Sie dann auf **Optionen**).</span><span class="sxs-lookup"><span data-stu-id="5c18e-115">You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="5c18e-116">Wenn Sie einen Verweis auf die Zelle ShdwPattern nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5c18e-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c18e-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5c18e-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5c18e-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="5c18e-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="5c18e-119">Wenn Sie einen Verweis auf die Zelle ShdwPattern aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5c18e-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c18e-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5c18e-120">Section index:</span></span>  <br/> |<span data-ttu-id="5c18e-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c18e-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5c18e-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5c18e-122">Row index:</span></span>  <br/> |<span data-ttu-id="5c18e-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="5c18e-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="5c18e-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5c18e-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5c18e-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="5c18e-125">**visFillShdwPattern**</span></span> <br/> |
   

