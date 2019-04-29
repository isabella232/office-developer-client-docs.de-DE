---
title: Zelle "DirX / A" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Bestimmt die x-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Die Zelle DirX/A wird auch verwendet, um den angefügten Teil eines dynamischen Konnektors auszurichten. Diese Zelle akzeptiert einen Fließkommawert.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422397"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="f8df0-105">Zelle "DirX / A" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="f8df0-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="f8df0-106">Bestimmt die *x* -Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts.</span><span class="sxs-lookup"><span data-stu-id="f8df0-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="f8df0-107">Die Zelle DirX/A wird auch verwendet, um den angefügten Teil eines dynamischen Konnektors auszurichten.</span><span class="sxs-lookup"><span data-stu-id="f8df0-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="f8df0-108">Diese Zelle benötigt einen Fließkommawert.</span><span class="sxs-lookup"><span data-stu-id="f8df0-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f8df0-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8df0-109">Remarks</span></span>

<span data-ttu-id="f8df0-110">Wenn Sie einen Verweis auf die Zelle DirX/A aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f8df0-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8df0-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f8df0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f8df0-112">Connections. DirX [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f8df0-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f8df0-113">Wenn Sie einen Verweis auf die Zelle DirX/A aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f8df0-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8df0-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f8df0-114">Section index:</span></span>  <br/> |<span data-ttu-id="f8df0-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="f8df0-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="f8df0-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f8df0-116">Row index:</span></span>  <br/> |<span data-ttu-id="f8df0-117">**visRowConnectionPts** +  *i* , wobei *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="f8df0-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="f8df0-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f8df0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f8df0-119">**visCnnctDirX** (nicht erweiterte Zeilen)           **visCnnctA** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="f8df0-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="f8df0-120">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="f8df0-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

