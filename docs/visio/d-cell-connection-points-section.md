---
title: Zelle "D" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796773"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="72bf9-103">D Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="72bf9-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="72bf9-104">Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="72bf9-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="72bf9-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72bf9-105">Remarks</span></span>

<span data-ttu-id="72bf9-106">Um auf die Zelle D zuzugreifen, klicken Sie mit der rechten Maustaste auf eine Zeile und anschließend im Kontextmenü auf Zeilentyp ändern.</span><span class="sxs-lookup"><span data-stu-id="72bf9-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="72bf9-107">Wenn Sie eine Referenz auf die Zelle D nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="72bf9-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72bf9-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="72bf9-108">Cell name:</span></span>  <br/> | <span data-ttu-id="72bf9-109">Connections.D [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="72bf9-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="72bf9-110">Wenn Sie eine Referenz auf die Zelle D aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="72bf9-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72bf9-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="72bf9-111">Section index:</span></span>  <br/> |<span data-ttu-id="72bf9-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="72bf9-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="72bf9-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="72bf9-113">Row index:</span></span>  <br/> |<span data-ttu-id="72bf9-114">**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="72bf9-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="72bf9-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="72bf9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="72bf9-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="72bf9-116">**visCnnctD**</span></span> <br/> |
   

