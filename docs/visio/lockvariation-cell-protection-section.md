---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die Design-Variante, die auf dem Zeichenblatt oder Shape angewendet, als ein boolescher Wert, geändert werden kann.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797418"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="7c462-103">LockVariation Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="7c462-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="7c462-104">Bestimmt, ob die Design-Variante, die auf dem Zeichenblatt oder Shape angewendet, als ein boolescher Wert, geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c462-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c462-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="7c462-105">TRUE</span></span>  <br/> |<span data-ttu-id="7c462-106">Die aktuelle Variation auf dem Zeichenblatt oder Shape angewendet kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7c462-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="7c462-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="7c462-107">FALSE</span></span>  <br/> |<span data-ttu-id="7c462-108">Die Variante des Zeichenblatts oder des Shape kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7c462-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c462-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c462-109">Remarks</span></span>

<span data-ttu-id="7c462-110">Wenn Sie einen Verweis auf die Zelle **LockVariation** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7c462-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c462-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7c462-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7c462-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="7c462-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="7c462-113">Wenn Sie einen Verweis auf die Zelle **LockVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7c462-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c462-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7c462-114">Section index:</span></span>  <br/> |<span data-ttu-id="7c462-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7c462-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7c462-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7c462-116">Row index:</span></span>  <br/> |<span data-ttu-id="7c462-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="7c462-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="7c462-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7c462-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7c462-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="7c462-119">**visLockVariation**</span></span> <br/> |
   

