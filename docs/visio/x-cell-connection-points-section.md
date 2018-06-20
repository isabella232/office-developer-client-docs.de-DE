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
description: Stellt die X-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798428"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="79a7c-103">X Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="79a7c-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="79a7c-104">Stellt die *X* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="79a7c-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="79a7c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79a7c-105">Remarks</span></span>

<span data-ttu-id="79a7c-106">Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="79a7c-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79a7c-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="79a7c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="79a7c-108">Connections.X *i* wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="79a7c-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="79a7c-109">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="79a7c-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79a7c-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="79a7c-110">Section index:</span></span>  <br/> |<span data-ttu-id="79a7c-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="79a7c-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="79a7c-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="79a7c-112">Row index:</span></span>  <br/> |<span data-ttu-id="79a7c-113">**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="79a7c-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="79a7c-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="79a7c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="79a7c-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="79a7c-115">**visX**</span></span> <br/> |
   

