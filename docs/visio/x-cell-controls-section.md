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
description: Stellt die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269783"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="a88a4-103">Zelle "X" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="a88a4-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="a88a4-104">Stellt die *x* -Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.</span><span class="sxs-lookup"><span data-stu-id="a88a4-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a88a4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a88a4-105">Remarks</span></span>

<span data-ttu-id="a88a4-106">Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a88a4-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a88a4-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a88a4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a88a4-108">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a88a4-108">Controls.</span></span>  <span data-ttu-id="a88a4-109">*Name* . X, wobei Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a88a4-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="a88a4-110">*Name* ist der Name der Zeile Controls.</span><span class="sxs-lookup"><span data-stu-id="a88a4-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="a88a4-111">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a88a4-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a88a4-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a88a4-112">Section index:</span></span>  <br/> |<span data-ttu-id="a88a4-113">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="a88a4-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="a88a4-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a88a4-114">Row index:</span></span>  <br/> |<span data-ttu-id="a88a4-115">**visRowControl** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a88a4-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a88a4-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a88a4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a88a4-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="a88a4-117">**visCtlX**</span></span> <br/> |
   

