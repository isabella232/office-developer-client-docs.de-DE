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
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797224"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="442c0-103">IsDropSource Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="442c0-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="442c0-104">Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="442c0-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="442c0-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="442c0-105">**Value**</span></span>|<span data-ttu-id="442c0-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="442c0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="442c0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="442c0-107">TRUE</span></span>  <br/> |<span data-ttu-id="442c0-108">Das Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="442c0-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="442c0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="442c0-109">FALSE</span></span>  <br/> |<span data-ttu-id="442c0-110">Das Shape kann einer Gruppe nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="442c0-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="442c0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="442c0-111">Remarks</span></span>

<span data-ttu-id="442c0-112">Sie können diesen Wert auch festlegen, indem Sie das Shape auswählen, auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** und dann auswählen das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="442c0-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="442c0-113">Neben der Aktivierung dieses Verhalten für ein Shape, müssen Sie auch eine Gruppe Shapes annehmen, die hinein gezogen werden aktivieren.</span><span class="sxs-lookup"><span data-stu-id="442c0-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="442c0-114">Dazu wählen Sie die Gruppe aus, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** , und wählen Sie dann das Kontrollkästchen **abgelegte Shapes annehmen** .</span><span class="sxs-lookup"><span data-stu-id="442c0-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="442c0-115">Dieser Wert wird in der Zelle IsDropTarget im Abschnitt Group Properties gespeichert.</span><span class="sxs-lookup"><span data-stu-id="442c0-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="442c0-116">Wenn Sie einen Verweis auf die Zelle IsDropSource nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="442c0-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="442c0-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="442c0-117">Cell name:</span></span>  <br/> |<span data-ttu-id="442c0-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="442c0-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="442c0-119">Wenn Sie einen Verweis auf die Zelle IsDropSource aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="442c0-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="442c0-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="442c0-120">Section index:</span></span>  <br/> |<span data-ttu-id="442c0-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="442c0-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="442c0-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="442c0-122">Row index:</span></span>  <br/> |<span data-ttu-id="442c0-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="442c0-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="442c0-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="442c0-124">Cell index:</span></span>  <br/> |<span data-ttu-id="442c0-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="442c0-125">**visDropSource**</span></span> <br/> |
   

