---
title: Zelle "X" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Represents the x -coordinate that indicates the location of a shape's control handle in local coordinates.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406451"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="06001-103">Zelle "X" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="06001-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="06001-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span><span class="sxs-lookup"><span data-stu-id="06001-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="06001-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06001-105">Remarks</span></span>

<span data-ttu-id="06001-106">Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="06001-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06001-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="06001-107">Cell name:</span></span>  <br/> | <span data-ttu-id="06001-108">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="06001-108">Controls.</span></span>  <span data-ttu-id="06001-109">*Name*  . X, wobei Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="06001-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="06001-110">*name*  ist der Name der Steuerelementzeile.</span><span class="sxs-lookup"><span data-stu-id="06001-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="06001-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="06001-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06001-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="06001-112">Section index:</span></span>  <br/> |<span data-ttu-id="06001-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="06001-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="06001-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="06001-114">Row index:</span></span>  <br/> |<span data-ttu-id="06001-115">**visRowControl**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="06001-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="06001-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="06001-116">Cell index:</span></span>  <br/> |<span data-ttu-id="06001-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="06001-117">**visCtlX**</span></span> <br/> |
   

