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
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="747d1-103">Zelle "SelectMode" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="747d1-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="747d1-104">Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.</span><span class="sxs-lookup"><span data-stu-id="747d1-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="747d1-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="747d1-105">**Value**</span></span>|<span data-ttu-id="747d1-106">**Auswahlmodus**</span><span class="sxs-lookup"><span data-stu-id="747d1-106">**Selection mode**</span></span>|<span data-ttu-id="747d1-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="747d1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="747d1-108">0</span><span class="sxs-lookup"><span data-stu-id="747d1-108">0</span></span>  <br/> |<span data-ttu-id="747d1-109">Nur das Gruppen-Shape auswählen.</span><span class="sxs-lookup"><span data-stu-id="747d1-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="747d1-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="747d1-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="747d1-111">1</span><span class="sxs-lookup"><span data-stu-id="747d1-111">1</span></span>  <br/> |<span data-ttu-id="747d1-112">Das Gruppen-Shape zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="747d1-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="747d1-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="747d1-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="747d1-114">2</span><span class="sxs-lookup"><span data-stu-id="747d1-114">2</span></span>  <br/> |<span data-ttu-id="747d1-115">Mitglieder der Gruppe zuerst auswählen.</span><span class="sxs-lookup"><span data-stu-id="747d1-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="747d1-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="747d1-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="747d1-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="747d1-117">Remarks</span></span>

<span data-ttu-id="747d1-118">Sie können diesen Wert  auch im Dialogfeld Verhalten festlegen (wenn [](run-in-developer-mode-display-the-developer-tab.md) die Gruppenform ausgewählt ist, klicken Sie auf der Registerkarte  Entwickler in der **Gruppe Shape-Entwurf** auf **Verhalten,** und klicken Sie dann unter Gruppenverhalten auf einen Modus in der Liste **Auswahl).**</span><span class="sxs-lookup"><span data-stu-id="747d1-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="747d1-119">Um einen Verweis auf die Zelle SelectMode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="747d1-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="747d1-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="747d1-120">Cell name:</span></span>  <br/> |<span data-ttu-id="747d1-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="747d1-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="747d1-122">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SelectMode nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="747d1-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="747d1-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="747d1-123">Section index:</span></span>  <br/> |<span data-ttu-id="747d1-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="747d1-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="747d1-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="747d1-125">Row index:</span></span>  <br/> |<span data-ttu-id="747d1-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="747d1-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="747d1-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="747d1-127">Cell index:</span></span>  <br/> |<span data-ttu-id="747d1-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="747d1-128">**visGroupSelectMode**</span></span> <br/> |
   

