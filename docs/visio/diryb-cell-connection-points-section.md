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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332585"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="5edd9-105">Zelle "DirY / B" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="5edd9-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="5edd9-106">Bestimmt die *y* -Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts.</span><span class="sxs-lookup"><span data-stu-id="5edd9-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="5edd9-107">Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet.</span><span class="sxs-lookup"><span data-stu-id="5edd9-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="5edd9-108">Diese Zelle benötigt einen Fließkommawert.</span><span class="sxs-lookup"><span data-stu-id="5edd9-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5edd9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5edd9-109">Remarks</span></span>

<span data-ttu-id="5edd9-110">Wenn Sie einen Verweis auf die Zelle DirY/B aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5edd9-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5edd9-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5edd9-111">Cell name:</span></span>  <br/> |<span data-ttu-id="5edd9-112">Connections. DirY [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5edd9-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5edd9-113">Wenn Sie einen Verweis auf die Zelle DirY/B aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5edd9-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5edd9-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5edd9-114">Section index:</span></span>  <br/> |<span data-ttu-id="5edd9-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="5edd9-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="5edd9-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5edd9-116">Row index:</span></span>  <br/> |<span data-ttu-id="5edd9-117">**visRowConnectionPts** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5edd9-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5edd9-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5edd9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5edd9-119">**visCnnctDirY** (nicht erweiterte Zeilen)           **visCnnctB** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="5edd9-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="5edd9-120">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="5edd9-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

