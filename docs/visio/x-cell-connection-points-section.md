---
title: Zelle "X" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Stellt die x-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436783"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="89e7c-103">Zelle "X" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="89e7c-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="89e7c-104">Stellt  die x-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="89e7c-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89e7c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89e7c-105">Remarks</span></span>

<span data-ttu-id="89e7c-106">Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="89e7c-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89e7c-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="89e7c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="89e7c-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="89e7c-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="89e7c-109">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="89e7c-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89e7c-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="89e7c-110">Section index:</span></span>  <br/> |<span data-ttu-id="89e7c-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="89e7c-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="89e7c-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="89e7c-112">Row index:</span></span>  <br/> |<span data-ttu-id="89e7c-113">**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="89e7c-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="89e7c-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="89e7c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="89e7c-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="89e7c-115">**visX**</span></span> <br/> |
   

