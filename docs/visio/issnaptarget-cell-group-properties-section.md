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
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421445"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="05cc8-103">Zelle "IsSnapTarget" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="05cc8-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="05cc8-104">Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="05cc8-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="05cc8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="05cc8-105">**Value**</span></span>|<span data-ttu-id="05cc8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05cc8-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05cc8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="05cc8-107">TRUE</span></span>  <br/> |<span data-ttu-id="05cc8-108">Einrasten an Shapes in einer Gruppe aktivieren.</span><span class="sxs-lookup"><span data-stu-id="05cc8-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="05cc8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="05cc8-109">FALSE</span></span>  <br/> |<span data-ttu-id="05cc8-110">Nur an der Gruppe einrasten.</span><span class="sxs-lookup"><span data-stu-id="05cc8-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05cc8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05cc8-111">Remarks</span></span>

<span data-ttu-id="05cc8-112">Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **An Mitglieds-Shapes einrasten** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="05cc8-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="05cc8-113">Verwenden Sie folgendes, um einen Verweis auf die Zelle IsSnapTarget anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="05cc8-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05cc8-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="05cc8-114">Cell name:</span></span>  <br/> |<span data-ttu-id="05cc8-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="05cc8-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="05cc8-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IsSnapTarget-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="05cc8-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05cc8-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="05cc8-117">Section index:</span></span>  <br/> |<span data-ttu-id="05cc8-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05cc8-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="05cc8-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="05cc8-119">Row index:</span></span>  <br/> |<span data-ttu-id="05cc8-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="05cc8-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="05cc8-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="05cc8-121">Cell index:</span></span>  <br/> |<span data-ttu-id="05cc8-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="05cc8-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

