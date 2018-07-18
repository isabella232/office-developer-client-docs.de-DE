---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Bestimmt den Typ der Schnellformatvorlagen (2-dimensionale, 1-dimensionales oder Connector), die das Shape erbt.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797760"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="91a6c-103">QuickStyleType Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="91a6c-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="91a6c-104">Bestimmt den Typ der Schnellformatvorlagen (2-dimensionale, 1-dimensionales oder Connector), die das Shape erbt.</span><span class="sxs-lookup"><span data-stu-id="91a6c-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="91a6c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="91a6c-105">**Value**</span></span>|<span data-ttu-id="91a6c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91a6c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91a6c-107">0</span><span class="sxs-lookup"><span data-stu-id="91a6c-107">0</span></span>  <br/> |<span data-ttu-id="91a6c-108">Visio wählt automatisch</span><span class="sxs-lookup"><span data-stu-id="91a6c-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="91a6c-109">1</span><span class="sxs-lookup"><span data-stu-id="91a6c-109">1</span></span>  <br/> |<span data-ttu-id="91a6c-110">1-dimensionales</span><span class="sxs-lookup"><span data-stu-id="91a6c-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="91a6c-111">2</span><span class="sxs-lookup"><span data-stu-id="91a6c-111">2</span></span>  <br/> |<span data-ttu-id="91a6c-112">2-dimensionale</span><span class="sxs-lookup"><span data-stu-id="91a6c-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="91a6c-113">3</span><span class="sxs-lookup"><span data-stu-id="91a6c-113">3</span></span>  <br/> |<span data-ttu-id="91a6c-114">Connector</span><span class="sxs-lookup"><span data-stu-id="91a6c-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91a6c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91a6c-115">Remarks</span></span>

<span data-ttu-id="91a6c-116">Wenn Sie einen Verweis auf die Zelle **QuickStyleType** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="91a6c-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91a6c-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="91a6c-117">Cell name:</span></span>  <br/> | <span data-ttu-id="91a6c-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="91a6c-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="91a6c-119">Wenn Sie einen Verweis auf die Zelle **QuickStyleType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="91a6c-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91a6c-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="91a6c-120">Section index:</span></span>  <br/> |<span data-ttu-id="91a6c-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91a6c-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="91a6c-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="91a6c-122">Row index:</span></span>  <br/> |<span data-ttu-id="91a6c-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="91a6c-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="91a6c-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="91a6c-124">Cell index:</span></span>  <br/> |<span data-ttu-id="91a6c-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="91a6c-125">**visQuickStyleType**</span></span> <br/> |
   

