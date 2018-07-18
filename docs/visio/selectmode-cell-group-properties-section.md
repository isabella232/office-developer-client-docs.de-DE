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
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797986"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="d8117-103">SelectMode Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="d8117-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="d8117-104">Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.</span><span class="sxs-lookup"><span data-stu-id="d8117-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="d8117-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d8117-105">**Value**</span></span>|<span data-ttu-id="d8117-106">**Markierungsmodus**</span><span class="sxs-lookup"><span data-stu-id="d8117-106">**Selection mode**</span></span>|<span data-ttu-id="d8117-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="d8117-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8117-108">0</span><span class="sxs-lookup"><span data-stu-id="d8117-108">0</span></span>  <br/> |<span data-ttu-id="d8117-109">Nur das Gruppen-Shape auswählen.</span><span class="sxs-lookup"><span data-stu-id="d8117-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="d8117-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="d8117-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="d8117-111">1</span><span class="sxs-lookup"><span data-stu-id="d8117-111">1</span></span>  <br/> |<span data-ttu-id="d8117-112">Das Gruppen-Shape zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="d8117-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="d8117-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="d8117-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="d8117-114">2</span><span class="sxs-lookup"><span data-stu-id="d8117-114">2</span></span>  <br/> |<span data-ttu-id="d8117-115">Mitglieder der Gruppe zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="d8117-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="d8117-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="d8117-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8117-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8117-117">Remarks</span></span>

<span data-ttu-id="d8117-118">Sie können diesen Wert auch im Dialogfeld **Verhalten** festlegen (mit das Gruppen-Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**und klicken Sie dann auf einen Modus in der Liste **Auswahl** unter **Gruppe Verhalten** ).</span><span class="sxs-lookup"><span data-stu-id="d8117-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="d8117-119">Wenn Sie einen Verweis auf die Zelle SelectMode aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d8117-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8117-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d8117-120">Cell name:</span></span>  <br/> |<span data-ttu-id="d8117-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="d8117-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="d8117-122">Wenn Sie einen Verweis auf die Zelle SelectMode aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d8117-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8117-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d8117-123">Section index:</span></span>  <br/> |<span data-ttu-id="d8117-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d8117-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d8117-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d8117-125">Row index:</span></span>  <br/> |<span data-ttu-id="d8117-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="d8117-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="d8117-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d8117-127">Cell index:</span></span>  <br/> |<span data-ttu-id="d8117-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="d8117-128">**visGroupSelectMode**</span></span> <br/> |
   

