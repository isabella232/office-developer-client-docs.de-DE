---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Bestimmt, ob für eine Linie oder den Rahmen eines Shapes ein Linie Farbverlauf aktiviert ist.
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797316"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="16aa3-103">LineGradientEnabled Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="16aa3-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="16aa3-104">Bestimmt, ob für eine Linie oder den Rahmen eines Shapes ein Linie Farbverlauf aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="16aa3-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="16aa3-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="16aa3-105">**Value**</span></span>|<span data-ttu-id="16aa3-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16aa3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16aa3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="16aa3-107">TRUE</span></span>  <br/> |<span data-ttu-id="16aa3-108">Farbverlauf wird in einer Zeile oder den Rahmen einer Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="16aa3-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="16aa3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="16aa3-109">FALSE</span></span>  <br/> |<span data-ttu-id="16aa3-110">Verläufe werden nicht in einer Zeile oder den Rahmen einer Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="16aa3-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16aa3-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16aa3-111">Remarks</span></span>

<span data-ttu-id="16aa3-112">Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16aa3-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16aa3-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="16aa3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="16aa3-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="16aa3-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="16aa3-115">Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="16aa3-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16aa3-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="16aa3-116">Section index:</span></span>  <br/> |<span data-ttu-id="16aa3-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16aa3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16aa3-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="16aa3-118">Row index:</span></span>  <br/> |<span data-ttu-id="16aa3-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="16aa3-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="16aa3-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="16aa3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="16aa3-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="16aa3-121">**visLineGradientEnabled**</span></span> <br/> |
   

