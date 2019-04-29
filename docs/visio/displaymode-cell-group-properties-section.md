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
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="03b5b-103">Zelle "DisplayMode" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="03b5b-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="03b5b-104">Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="03b5b-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="03b5b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="03b5b-105">**Value**</span></span>|<span data-ttu-id="03b5b-106">**Anzeigemodus**</span><span class="sxs-lookup"><span data-stu-id="03b5b-106">**Display Mode**</span></span>|<span data-ttu-id="03b5b-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="03b5b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03b5b-108">0</span><span class="sxs-lookup"><span data-stu-id="03b5b-108">0</span></span>  <br/> |<span data-ttu-id="03b5b-109">Blendet das Gruppen-Shape und den Text aus.</span><span class="sxs-lookup"><span data-stu-id="03b5b-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="03b5b-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="03b5b-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="03b5b-111">1</span><span class="sxs-lookup"><span data-stu-id="03b5b-111">1</span></span>  <br/> |<span data-ttu-id="03b5b-112">Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.</span><span class="sxs-lookup"><span data-stu-id="03b5b-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="03b5b-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="03b5b-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="03b5b-114">2</span><span class="sxs-lookup"><span data-stu-id="03b5b-114">2</span></span>  <br/> |<span data-ttu-id="03b5b-115">Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.</span><span class="sxs-lookup"><span data-stu-id="03b5b-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="03b5b-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="03b5b-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03b5b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03b5b-117">Remarks</span></span>

<span data-ttu-id="03b5b-118">Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten** klicken und dann in der **Gruppe Daten** Liste einen Anzeigemodus auswählen.</span><span class="sxs-lookup"><span data-stu-id="03b5b-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="03b5b-119">Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="03b5b-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03b5b-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="03b5b-120">Cell name:</span></span>  <br/> |<span data-ttu-id="03b5b-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="03b5b-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="03b5b-122">Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="03b5b-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03b5b-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="03b5b-123">Section index:</span></span>  <br/> |<span data-ttu-id="03b5b-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="03b5b-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="03b5b-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="03b5b-125">Row index:</span></span>  <br/> |<span data-ttu-id="03b5b-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="03b5b-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="03b5b-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="03b5b-127">Cell index:</span></span>  <br/> |<span data-ttu-id="03b5b-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="03b5b-128">**visGroupDisplayMode**</span></span> <br/> |
   

