---
title: Zelle "DisplayMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796854"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="b0ed4-103">Zelle "DisplayMode" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="b0ed4-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="b0ed4-104">Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="b0ed4-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-105">**Value**</span></span>|<span data-ttu-id="b0ed4-106">**Anzeigemodus**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-106">**Display Mode**</span></span>|<span data-ttu-id="b0ed4-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0ed4-108">0</span><span class="sxs-lookup"><span data-stu-id="b0ed4-108">0</span></span>  <br/> |<span data-ttu-id="b0ed4-109">Blendet das Gruppen-Shape und den Text aus.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="b0ed4-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="b0ed4-111">1</span><span class="sxs-lookup"><span data-stu-id="b0ed4-111">1</span></span>  <br/> |<span data-ttu-id="b0ed4-112">Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="b0ed4-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="b0ed4-114">2</span><span class="sxs-lookup"><span data-stu-id="b0ed4-114">2</span></span>  <br/> |<span data-ttu-id="b0ed4-115">Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="b0ed4-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0ed4-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0ed4-117">Remarks</span></span>

<span data-ttu-id="b0ed4-118">Sie können diesen Wert auch festlegen durch die Gruppe auswählen auf die Gruppe **Shape-Design** auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) **Verhalten** klicken und anschließend einen Anzeigemodus aus der Liste **Gruppe** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="b0ed4-119">Wenn Sie einen Verweis auf die Zelle DisplayMode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0ed4-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-120">Cell name:</span></span>  <br/> |<span data-ttu-id="b0ed4-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="b0ed4-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="b0ed4-122">Wenn Sie einen Verweis auf die Zelle DisplayMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0ed4-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-123">Section index:</span></span>  <br/> |<span data-ttu-id="b0ed4-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b0ed4-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-125">Row index:</span></span>  <br/> |<span data-ttu-id="b0ed4-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="b0ed4-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-127">Cell index:</span></span>  <br/> |<span data-ttu-id="b0ed4-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-128">**visGroupDisplayMode**</span></span> <br/> |
   

