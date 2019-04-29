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
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="dd54d-103">Zelle "NoShow" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="dd54d-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="dd54d-104">Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd54d-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="dd54d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dd54d-105">**Value**</span></span>|<span data-ttu-id="dd54d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd54d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dd54d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd54d-107">TRUE</span></span>  <br/> | <span data-ttu-id="dd54d-108">Der Strich und die Füllung des Pfads, der durch den Abschnitt dargestellt wird, sind ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="dd54d-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="dd54d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd54d-109">FALSE</span></span>  <br/> | <span data-ttu-id="dd54d-110">Der Strich und die Füllung des Pfades werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd54d-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd54d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd54d-111">Remarks</span></span>

<span data-ttu-id="dd54d-112">Wenn Sie einen Verweis auf die Zelle noShow aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dd54d-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd54d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dd54d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dd54d-114">Geometrie *i* . NoShow Where *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dd54d-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dd54d-115">Wenn Sie einen Verweis auf die Zelle noShow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dd54d-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd54d-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dd54d-116">Section index:</span></span>  <br/> |<span data-ttu-id="dd54d-117">**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dd54d-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dd54d-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dd54d-118">Row index:</span></span>  <br/> |<span data-ttu-id="dd54d-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="dd54d-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="dd54d-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dd54d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dd54d-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="dd54d-121">**visCompNoShow**</span></span> <br/> |
   

