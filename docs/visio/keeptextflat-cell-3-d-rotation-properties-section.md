---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob ein Shape-Text des Shapes Drehung in 3D ignoriert. Gilt nicht für 2D-Diagramme Drehung.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797267"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="d641b-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="d641b-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="d641b-105">Gibt an, ob ein Shape-Text des Shapes Drehung in 3D ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d641b-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="d641b-106">Gilt nicht für 2D-Diagramme Drehung.</span><span class="sxs-lookup"><span data-stu-id="d641b-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="d641b-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d641b-107">**Value**</span></span>|<span data-ttu-id="d641b-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d641b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d641b-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="d641b-109">TRUE</span></span>  <br/> |<span data-ttu-id="d641b-110">Shape-Text wird nicht mit der Shape-Geometrie gedreht.</span><span class="sxs-lookup"><span data-stu-id="d641b-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="d641b-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="d641b-111">FALSE</span></span>  <br/> |<span data-ttu-id="d641b-112">Shape-Text wird so gedreht mit der Shape-Geometrie umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="d641b-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d641b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d641b-113">Remarks</span></span>

<span data-ttu-id="d641b-114">Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d641b-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d641b-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d641b-115">Cell name:</span></span>  <br/> |<span data-ttu-id="d641b-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="d641b-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="d641b-117">Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d641b-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d641b-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d641b-118">Section index:</span></span>  <br/> |<span data-ttu-id="d641b-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d641b-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d641b-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d641b-120">Row index:</span></span>  <br/> |<span data-ttu-id="d641b-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="d641b-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="d641b-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d641b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d641b-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="d641b-123">**visKeepTextFlat**</span></span> <br/> |
   

