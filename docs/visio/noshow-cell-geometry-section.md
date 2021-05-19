---
title: Zelle "NoShow" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410350"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="41ac9-103">Zelle "NoShow" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="41ac9-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="41ac9-104">Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="41ac9-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="41ac9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="41ac9-105">**Value**</span></span>|<span data-ttu-id="41ac9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41ac9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="41ac9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="41ac9-107">TRUE</span></span>  <br/> | <span data-ttu-id="41ac9-108">Der Strich und die Füllung des Pfads, der durch den Abschnitt dargestellt wird, sind ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="41ac9-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="41ac9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="41ac9-109">FALSE</span></span>  <br/> | <span data-ttu-id="41ac9-110">Der Strich und die Füllung des Pfades werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41ac9-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41ac9-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41ac9-111">Remarks</span></span>

<span data-ttu-id="41ac9-112">Um einen Verweis auf die Zelle NoShow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="41ac9-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41ac9-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="41ac9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="41ac9-114">Geometry  *i*  . NoShow,  *wobei i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="41ac9-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="41ac9-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NoShow nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="41ac9-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41ac9-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="41ac9-116">Section index:</span></span>  <br/> |<span data-ttu-id="41ac9-117">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="41ac9-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="41ac9-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="41ac9-118">Row index:</span></span>  <br/> |<span data-ttu-id="41ac9-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="41ac9-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="41ac9-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="41ac9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="41ac9-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="41ac9-121">**visCompNoShow**</span></span> <br/> |
   

