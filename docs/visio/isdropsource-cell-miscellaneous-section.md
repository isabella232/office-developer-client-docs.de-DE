---
title: Zelle "IsDropSource" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421893"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="bc43f-103">Zelle "IsDropSource" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="bc43f-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="bc43f-104">Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc43f-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="bc43f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bc43f-105">**Value**</span></span>|<span data-ttu-id="bc43f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc43f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc43f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc43f-107">TRUE</span></span>  <br/> |<span data-ttu-id="bc43f-108">Das Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bc43f-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="bc43f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bc43f-109">FALSE</span></span>  <br/> |<span data-ttu-id="bc43f-110">Das Shape kann einer Gruppe nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bc43f-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc43f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc43f-111">Remarks</span></span>

<span data-ttu-id="bc43f-112">Sie können diesen Wert auch festlegen, indem Sie das Shape auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc43f-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="bc43f-113">Zusätzlich zum Aktivieren dieses Verhaltens für ein Shape müssen Sie eine Gruppe auch zum Akzeptieren von Shapes aktivieren, die in dieses Shape gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="bc43f-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="bc43f-114">Wählen Sie dazu die Gruppe aus, [](run-in-developer-mode-display-the-developer-tab.md) **klicken** Sie auf der Registerkarte Entwickler auf Verhalten, und aktivieren Sie dann das Kontrollkästchen **Verworfene Shapes** akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="bc43f-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="bc43f-115">Dieser Wert wird in der Zelle IsDropTarget im Abschnitt Gruppeneigenschaften gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bc43f-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="bc43f-116">Um einen Verweis auf die Zelle IsDropSource anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="bc43f-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc43f-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bc43f-117">Cell name:</span></span>  <br/> |<span data-ttu-id="bc43f-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="bc43f-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="bc43f-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IsDropSource-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bc43f-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc43f-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bc43f-120">Section index:</span></span>  <br/> |<span data-ttu-id="bc43f-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bc43f-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bc43f-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bc43f-122">Row index:</span></span>  <br/> |<span data-ttu-id="bc43f-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="bc43f-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="bc43f-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bc43f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="bc43f-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="bc43f-125">**visDropSource**</span></span> <br/> |
   

