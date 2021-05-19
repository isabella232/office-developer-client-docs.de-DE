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
description: Bestimmt die y-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417091"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="fbd90-105">Zelle "DirY / B" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="fbd90-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="fbd90-106">Bestimmt die  *y-Komponente*  für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts.</span><span class="sxs-lookup"><span data-stu-id="fbd90-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="fbd90-107">Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbd90-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="fbd90-108">Diese Zelle benötigt einen Fließkommawert.</span><span class="sxs-lookup"><span data-stu-id="fbd90-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fbd90-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbd90-109">Remarks</span></span>

<span data-ttu-id="fbd90-110">Verwenden Sie zum Erhalten eines Verweises auf die Zelle DirY/B anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="fbd90-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbd90-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fbd90-111">Cell name:</span></span>  <br/> |<span data-ttu-id="fbd90-112">Connections.DirY[ *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fbd90-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fbd90-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DirY/B nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="fbd90-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbd90-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fbd90-114">Section index:</span></span>  <br/> |<span data-ttu-id="fbd90-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="fbd90-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="fbd90-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fbd90-116">Row index:</span></span>  <br/> |<span data-ttu-id="fbd90-117">**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fbd90-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fbd90-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fbd90-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fbd90-119">**visCnnctDirY** (nicht erweiterte Zeilen)           **visCnnctB** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="fbd90-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="fbd90-120">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="fbd90-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

