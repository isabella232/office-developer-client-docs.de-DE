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
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413185"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="7a34c-103">Zelle "DisplayMode" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="7a34c-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="7a34c-104">Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7a34c-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="7a34c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7a34c-105">**Value**</span></span>|<span data-ttu-id="7a34c-106">**Anzeigemodus**</span><span class="sxs-lookup"><span data-stu-id="7a34c-106">**Display Mode**</span></span>|<span data-ttu-id="7a34c-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="7a34c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a34c-108">0</span><span class="sxs-lookup"><span data-stu-id="7a34c-108">0</span></span>  <br/> |<span data-ttu-id="7a34c-109">Blendet das Gruppen-Shape und den Text aus.</span><span class="sxs-lookup"><span data-stu-id="7a34c-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="7a34c-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="7a34c-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="7a34c-111">1</span><span class="sxs-lookup"><span data-stu-id="7a34c-111">1</span></span>  <br/> |<span data-ttu-id="7a34c-112">Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.</span><span class="sxs-lookup"><span data-stu-id="7a34c-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="7a34c-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="7a34c-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="7a34c-114">2</span><span class="sxs-lookup"><span data-stu-id="7a34c-114">2</span></span>  <br/> |<span data-ttu-id="7a34c-115">Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.</span><span class="sxs-lookup"><span data-stu-id="7a34c-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="7a34c-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="7a34c-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a34c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a34c-117">Remarks</span></span>

<span data-ttu-id="7a34c-118">Sie können diesen Wert auch festlegen,  indem Sie die Gruppe [](run-in-developer-mode-display-the-developer-tab.md) auswählen, auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf Verhalten klicken und dann in der Datenliste Gruppe einen Anzeigemodus **auswählen.**</span><span class="sxs-lookup"><span data-stu-id="7a34c-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="7a34c-119">Um einen Verweis auf die Zelle DisplayMode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="7a34c-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a34c-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7a34c-120">Cell name:</span></span>  <br/> |<span data-ttu-id="7a34c-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="7a34c-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="7a34c-122">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DisplayMode nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="7a34c-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a34c-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7a34c-123">Section index:</span></span>  <br/> |<span data-ttu-id="7a34c-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7a34c-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7a34c-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7a34c-125">Row index:</span></span>  <br/> |<span data-ttu-id="7a34c-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="7a34c-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="7a34c-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7a34c-127">Cell index:</span></span>  <br/> |<span data-ttu-id="7a34c-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="7a34c-128">**visGroupDisplayMode**</span></span> <br/> |
   

