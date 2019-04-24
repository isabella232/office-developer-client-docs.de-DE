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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326012"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="dd3d2-103">Zelle "SelectMode" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="dd3d2-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="dd3d2-104">Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd3d2-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="dd3d2-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-105">**Value**</span></span>|<span data-ttu-id="dd3d2-106">**Auswahlmodus**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-106">**Selection mode**</span></span>|<span data-ttu-id="dd3d2-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd3d2-108">0</span><span class="sxs-lookup"><span data-stu-id="dd3d2-108">0</span></span>  <br/> |<span data-ttu-id="dd3d2-109">Nur das Gruppen-Shape auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd3d2-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="dd3d2-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="dd3d2-111">1</span><span class="sxs-lookup"><span data-stu-id="dd3d2-111">1</span></span>  <br/> |<span data-ttu-id="dd3d2-112">Das Gruppen-Shape zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd3d2-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="dd3d2-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="dd3d2-114">2</span><span class="sxs-lookup"><span data-stu-id="dd3d2-114">2</span></span>  <br/> |<span data-ttu-id="dd3d2-115">Mitglieder der Gruppe zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd3d2-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="dd3d2-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd3d2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd3d2-117">Remarks</span></span>

<span data-ttu-id="dd3d2-118">Sie können diesen Wert auch im Dialogfeld **Verhalten** festlegen (wenn das Gruppen-Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann in der **Auswahl** Liste Untergruppe auf einen Modus. \*\* Verhalten\*\* ).</span><span class="sxs-lookup"><span data-stu-id="dd3d2-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="dd3d2-119">Wenn Sie einen Verweis auf die Zelle "SelectMode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dd3d2-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd3d2-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dd3d2-120">Cell name:</span></span>  <br/> |<span data-ttu-id="dd3d2-121">"SelectMode</span><span class="sxs-lookup"><span data-stu-id="dd3d2-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="dd3d2-122">Wenn Sie einen Verweis auf die Zelle "SelectMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dd3d2-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd3d2-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dd3d2-123">Section index:</span></span>  <br/> |<span data-ttu-id="dd3d2-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd3d2-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dd3d2-125">Row index:</span></span>  <br/> |<span data-ttu-id="dd3d2-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="dd3d2-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dd3d2-127">Cell index:</span></span>  <br/> |<span data-ttu-id="dd3d2-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="dd3d2-128">**visGroupSelectMode**</span></span> <br/> |
   

