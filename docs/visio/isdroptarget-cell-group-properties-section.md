---
title: Zelle "IsDropTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410791"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="043f6-103">Zelle "IsDropTarget" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="043f6-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="043f6-104">Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="043f6-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="043f6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="043f6-105">**Value**</span></span>|<span data-ttu-id="043f6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="043f6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="043f6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="043f6-107">TRUE</span></span>  <br/> |<span data-ttu-id="043f6-108">Ein Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="043f6-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="043f6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="043f6-109">FALSE</span></span>  <br/> |<span data-ttu-id="043f6-110">Das Shape kann auf der Gruppe nicht abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="043f6-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="043f6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="043f6-111">Remarks</span></span>

<span data-ttu-id="043f6-112">Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Abgelegte Shapes annehmen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="043f6-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="043f6-113">Um einer Gruppe ein Shape hinzuzufügen, indem Sie es in der Gruppe ablegen, müssen Sie auch ein ähnliches Formverhalten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="043f6-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="043f6-114">Sie müssen das Shape auswählen, [](run-in-developer-mode-display-the-developer-tab.md) **auf** der Registerkarte Entwickler auf Verhalten klicken und dann das Kontrollkästchen Shape zu Gruppen bei der **Dropdownliste** hinzufügen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="043f6-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="043f6-115">Dieser Wert wird in der Zelle IsDropSource im Abschnitt Verschiedene gespeichert.</span><span class="sxs-lookup"><span data-stu-id="043f6-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="043f6-116">Verwenden Sie folgendes, um einen Verweis auf die Zelle IsDropTarget anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="043f6-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="043f6-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="043f6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="043f6-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="043f6-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="043f6-119">Um einen Verweis auf die IsDropTarget-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="043f6-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="043f6-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="043f6-120">Section index:</span></span>  <br/> |<span data-ttu-id="043f6-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="043f6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="043f6-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="043f6-122">Row index:</span></span>  <br/> |<span data-ttu-id="043f6-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="043f6-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="043f6-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="043f6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="043f6-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="043f6-125">**visGroupIsDropTarget**</span></span> <br/> |
   

