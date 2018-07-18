---
title: Zelle "Y" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Stellt die y-Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798453"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="e89a8-103">Y Cell (Controls Section)</span><span class="sxs-lookup"><span data-stu-id="e89a8-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="e89a8-104">Stellt die *y* -Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e89a8-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e89a8-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e89a8-105">Remarks</span></span>

<span data-ttu-id="e89a8-106">Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e89a8-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e89a8-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e89a8-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e89a8-108">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e89a8-108">Controls.</span></span>  <span data-ttu-id="e89a8-109">*Name* . Ywhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e89a8-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="e89a8-110">*Name* ist der Name der Zeile mit Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="e89a8-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="e89a8-111">Wenn Sie einen Verweis auf die Zelle Y aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e89a8-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e89a8-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e89a8-112">Section index:</span></span>  <br/> |<span data-ttu-id="e89a8-113">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="e89a8-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="e89a8-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e89a8-114">Row index:</span></span>  <br/> |<span data-ttu-id="e89a8-115">**VisRowControl** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e89a8-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e89a8-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e89a8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e89a8-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="e89a8-117">**visCtlY**</span></span> <br/> |
   

