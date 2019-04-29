---
title: Zelle "Lock" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Gibt an, ob die dem Layer zugehörigen Shapes gesperrt sind, damit sie nicht ausgewählt oder bearbeitet werden können.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438827"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="15757-103">Zelle "Lock" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="15757-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="15757-104">Gibt an, ob die dem Layer zugehörigen Shapes gesperrt sind, damit sie nicht ausgewählt oder bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="15757-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="15757-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="15757-105">**Value**</span></span>|<span data-ttu-id="15757-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15757-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15757-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="15757-107">TRUE</span></span>  <br/> |<span data-ttu-id="15757-108">Shapes sind gesperrt.</span><span class="sxs-lookup"><span data-stu-id="15757-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="15757-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="15757-109">FALSE</span></span>  <br/> |<span data-ttu-id="15757-110">Shapes sind nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="15757-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15757-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15757-111">Remarks</span></span>

<span data-ttu-id="15757-112">Sie können diesen Wert auch festlegen, indem Sie im Dialogfeld **Layereigenschaften** die Option **Sperre** aktivieren (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="15757-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="15757-113">Wenn Sie einen Verweis auf die Zelle Lock aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="15757-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15757-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="15757-114">Cell name:</span></span>  <br/> |<span data-ttu-id="15757-115">Layers. Locked [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="15757-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="15757-116">Wenn Sie einen Verweis auf die Zelle Lock aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="15757-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15757-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="15757-117">Section index:</span></span>  <br/> |<span data-ttu-id="15757-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="15757-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="15757-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="15757-119">Row index:</span></span>  <br/> |<span data-ttu-id="15757-120">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="15757-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="15757-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="15757-121">Cell index:</span></span>  <br/> |<span data-ttu-id="15757-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="15757-122">**visLayerLock**</span></span> <br/> |
   

