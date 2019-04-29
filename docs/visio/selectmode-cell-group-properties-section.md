---
title: Zelle "SelectMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435362"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="e148e-103">Zelle "SelectMode" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="e148e-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="e148e-104">Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.</span><span class="sxs-lookup"><span data-stu-id="e148e-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="e148e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e148e-105">**Value**</span></span>|<span data-ttu-id="e148e-106">**Auswahlmodus**</span><span class="sxs-lookup"><span data-stu-id="e148e-106">**Selection mode**</span></span>|<span data-ttu-id="e148e-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="e148e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e148e-108">0</span><span class="sxs-lookup"><span data-stu-id="e148e-108">0</span></span>  <br/> |<span data-ttu-id="e148e-109">Nur das Gruppen-Shape auswählen.</span><span class="sxs-lookup"><span data-stu-id="e148e-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="e148e-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="e148e-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="e148e-111">1</span><span class="sxs-lookup"><span data-stu-id="e148e-111">1</span></span>  <br/> |<span data-ttu-id="e148e-112">Das Gruppen-Shape zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="e148e-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="e148e-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="e148e-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="e148e-114">2</span><span class="sxs-lookup"><span data-stu-id="e148e-114">2</span></span>  <br/> |<span data-ttu-id="e148e-115">Mitglieder der Gruppe zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="e148e-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="e148e-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="e148e-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e148e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e148e-117">Remarks</span></span>

<span data-ttu-id="e148e-118">Sie können diesen Wert auch im Dialogfeld **Verhalten** festlegen (wenn das Gruppen-Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann in der **Auswahl** Liste Untergruppe auf einen Modus. \*\* Verhalten\*\* ).</span><span class="sxs-lookup"><span data-stu-id="e148e-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="e148e-119">Wenn Sie einen Verweis auf die Zelle "SelectMode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e148e-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e148e-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e148e-120">Cell name:</span></span>  <br/> |<span data-ttu-id="e148e-121">"SelectMode</span><span class="sxs-lookup"><span data-stu-id="e148e-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="e148e-122">Wenn Sie einen Verweis auf die Zelle "SelectMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e148e-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e148e-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e148e-123">Section index:</span></span>  <br/> |<span data-ttu-id="e148e-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e148e-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e148e-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e148e-125">Row index:</span></span>  <br/> |<span data-ttu-id="e148e-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="e148e-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="e148e-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e148e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e148e-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="e148e-128">**visGroupSelectMode**</span></span> <br/> |
   

