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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416377"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="dcb94-103">Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="dcb94-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="dcb94-104">Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dcb94-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="dcb94-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dcb94-105">**Value**</span></span>|<span data-ttu-id="dcb94-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dcb94-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dcb94-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dcb94-107">TRUE</span></span>  <br/> |<span data-ttu-id="dcb94-108">Der Farbverlauf wird auf der Linie oder dem Rahmen einer Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dcb94-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="dcb94-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dcb94-109">FALSE</span></span>  <br/> |<span data-ttu-id="dcb94-110">Farbverläufe werden nicht auf der Linie oder dem Rahmen einer Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dcb94-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcb94-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcb94-111">Remarks</span></span>

<span data-ttu-id="dcb94-112">Um einen Verweis auf die **LineGradientEnabled-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="dcb94-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcb94-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dcb94-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dcb94-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="dcb94-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="dcb94-115">Um einen Verweis auf die **LineGradientEnabled-Zelle** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dcb94-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcb94-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dcb94-116">Section index:</span></span>  <br/> |<span data-ttu-id="dcb94-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dcb94-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dcb94-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dcb94-118">Row index:</span></span>  <br/> |<span data-ttu-id="dcb94-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="dcb94-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="dcb94-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dcb94-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dcb94-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="dcb94-121">**visLineGradientEnabled**</span></span> <br/> |
   

