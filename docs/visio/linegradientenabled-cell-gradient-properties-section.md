---
title: Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361138"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="b2d66-103">Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="b2d66-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="b2d66-104">Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b2d66-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="b2d66-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b2d66-105">**Value**</span></span>|<span data-ttu-id="b2d66-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2d66-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2d66-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2d66-107">TRUE</span></span>  <br/> |<span data-ttu-id="b2d66-108">Der Farbverlauf wird auf der Linie oder dem Rahmen eines Shapes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2d66-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="b2d66-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2d66-109">FALSE</span></span>  <br/> |<span data-ttu-id="b2d66-110">Farbverläufe werden nicht auf der Linie oder dem Rahmen eines Shapes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2d66-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2d66-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2d66-111">Remarks</span></span>

<span data-ttu-id="b2d66-112">Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b2d66-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2d66-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b2d66-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b2d66-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="b2d66-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="b2d66-115">Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b2d66-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2d66-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b2d66-116">Section index:</span></span>  <br/> |<span data-ttu-id="b2d66-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2d66-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b2d66-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b2d66-118">Row index:</span></span>  <br/> |<span data-ttu-id="b2d66-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="b2d66-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="b2d66-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b2d66-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b2d66-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="b2d66-121">**visLineGradientEnabled**</span></span> <br/> |
   

