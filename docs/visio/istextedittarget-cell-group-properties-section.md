---
title: Zelle "IsTextEditTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Definiert die Textzuweisung für eine Gruppe.
ms.openlocfilehash: 65baf90254f6b213efea04739d8e4a66952b2856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797262"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="a6af6-103">IsTextEditTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="a6af6-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="a6af6-104">Definiert die Textzuweisung für eine Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a6af6-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="a6af6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a6af6-105">**Value**</span></span>|<span data-ttu-id="a6af6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6af6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6af6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a6af6-107">TRUE</span></span>  <br/> |<span data-ttu-id="a6af6-108">Dem Gruppen-Shape wird Text hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a6af6-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="a6af6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a6af6-109">FALSE</span></span>  <br/> |<span data-ttu-id="a6af6-110">Text wird dem Shape in der obersten Gruppe des Stapels hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a6af6-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6af6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6af6-111">Remarks</span></span>

<span data-ttu-id="a6af6-112">Sie können diesen Wert auch festlegen, indem Auswählen der Gruppe auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) **Verhalten** klicken und anschließend das Kontrollkästchen **Text der Gruppe bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="a6af6-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="a6af6-p101">Bei Gruppen, die mit Versionen vor Visio 2000 erstellt wurden, ist der Standardwert FALSE vorgegeben. Ab Visio 2000-Versionen wird der Standardwert TRUE verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6af6-p101">Groups created in versions earlier than Visio 2000 have a default value of FALSE. Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="a6af6-115">Wenn Sie einen Verweis auf die Zelle IsTextEditTarget nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6af6-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6af6-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a6af6-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a6af6-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="a6af6-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="a6af6-118">Wenn Sie einen Verweis auf die Zelle IsTextEditTarget aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a6af6-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6af6-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a6af6-119">Section index:</span></span>  <br/> |<span data-ttu-id="a6af6-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6af6-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a6af6-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a6af6-121">Row index:</span></span>  <br/> |<span data-ttu-id="a6af6-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="a6af6-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="a6af6-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a6af6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a6af6-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="a6af6-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

