---
title: Zelle "IsSnapTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797249"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="00512-103">IsSnapTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="00512-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="00512-104">Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="00512-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="00512-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="00512-105">**Value**</span></span>|<span data-ttu-id="00512-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00512-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00512-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="00512-107">TRUE</span></span>  <br/> |<span data-ttu-id="00512-108">Einrasten an Shapes in einer Gruppe aktivieren.</span><span class="sxs-lookup"><span data-stu-id="00512-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="00512-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="00512-109">FALSE</span></span>  <br/> |<span data-ttu-id="00512-110">Nur an der Gruppe einrasten.</span><span class="sxs-lookup"><span data-stu-id="00512-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00512-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00512-111">Remarks</span></span>

<span data-ttu-id="00512-112">Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **An Mitglieds-Shapes einrasten** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="00512-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="00512-113">Wenn Sie einen Verweis auf die Zelle IsSnapTarget aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="00512-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00512-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="00512-114">Cell name:</span></span>  <br/> |<span data-ttu-id="00512-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="00512-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="00512-116">Wenn Sie einen Verweis auf die Zelle IsSnapTarget aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="00512-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00512-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="00512-117">Section index:</span></span>  <br/> |<span data-ttu-id="00512-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00512-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="00512-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="00512-119">Row index:</span></span>  <br/> |<span data-ttu-id="00512-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="00512-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="00512-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="00512-121">Cell index:</span></span>  <br/> |<span data-ttu-id="00512-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="00512-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

