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
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345087"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="d0584-103">Zelle "D" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="d0584-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="d0584-104">Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0584-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0584-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0584-105">Remarks</span></span>

<span data-ttu-id="d0584-106">Klicken Sie zum Zugreifen auf die Zelle D mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **zeilenTyp ändern** .</span><span class="sxs-lookup"><span data-stu-id="d0584-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="d0584-107">Wenn Sie einen Verweis auf die Zelle D aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d0584-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0584-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d0584-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d0584-109">Connections. D [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d0584-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d0584-110">Wenn Sie einen Verweis auf die Zelle D nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d0584-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0584-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d0584-111">Section index:</span></span>  <br/> |<span data-ttu-id="d0584-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="d0584-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="d0584-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d0584-113">Row index:</span></span>  <br/> |<span data-ttu-id="d0584-114">**visRowConnectionPts** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d0584-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d0584-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d0584-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d0584-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="d0584-116">**visCnnctD**</span></span> <br/> |
   

