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
description: Stellt die X-Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798433"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="71c70-103">Zelle "X" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="71c70-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="71c70-104">Stellt die *X* -Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.</span><span class="sxs-lookup"><span data-stu-id="71c70-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="71c70-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71c70-105">Remarks</span></span>

<span data-ttu-id="71c70-106">Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="71c70-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71c70-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="71c70-107">Cell name:</span></span>  <br/> | <span data-ttu-id="71c70-108">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="71c70-108">Controls.</span></span>  <span data-ttu-id="71c70-109">*Name* . X Where steuert.</span><span class="sxs-lookup"><span data-stu-id="71c70-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="71c70-110">*Name* ist der Name der Zeile mit Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="71c70-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="71c70-111">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="71c70-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71c70-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="71c70-112">Section index:</span></span>  <br/> |<span data-ttu-id="71c70-113">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="71c70-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="71c70-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="71c70-114">Row index:</span></span>  <br/> |<span data-ttu-id="71c70-115">**VisRowControl** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="71c70-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="71c70-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="71c70-116">Cell index:</span></span>  <br/> |<span data-ttu-id="71c70-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="71c70-117">**visCtlX**</span></span> <br/> |
   
