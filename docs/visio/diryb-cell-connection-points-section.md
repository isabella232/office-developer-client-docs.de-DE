---
title: Zelle "DirY / B" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Legt die y-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Es wird auch zum Ausrichten des verbundenen Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Gleitkommawert Codepunktwert.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796840"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="39d24-105">DirY / B Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="39d24-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="39d24-106">Legt die *y* -Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts.</span><span class="sxs-lookup"><span data-stu-id="39d24-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="39d24-107">Es wird auch zum Ausrichten des verbundenen Abschnitts eines dynamischen Verbinders verwendet.</span><span class="sxs-lookup"><span data-stu-id="39d24-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="39d24-108">Diese Zelle benötigt einen Gleitkommawert Codepunktwert.</span><span class="sxs-lookup"><span data-stu-id="39d24-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="39d24-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39d24-109">Remarks</span></span>

<span data-ttu-id="39d24-110">Wenn Sie einen Verweis auf die Zelle DirY / B aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="39d24-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39d24-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="39d24-111">Cell name:</span></span>  <br/> |<span data-ttu-id="39d24-112">Connections.DirY [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="39d24-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="39d24-113">Wenn Sie einen Verweis auf die Zelle DirY / B aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="39d24-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39d24-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="39d24-114">Section index:</span></span>  <br/> |<span data-ttu-id="39d24-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="39d24-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="39d24-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="39d24-116">Row index:</span></span>  <br/> |<span data-ttu-id="39d24-117">**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="39d24-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="39d24-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="39d24-118">Cell index:</span></span>  <br/> |<span data-ttu-id="39d24-119">**visCnnctDirY** (nicht erweiterte Zeilen)           **visCnnctB** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="39d24-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="39d24-120">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="39d24-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

