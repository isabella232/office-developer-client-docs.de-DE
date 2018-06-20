---
title: Zelle "Y" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Stellt die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798442"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="4efbc-103">Y Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="4efbc-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="4efbc-104">Stellt die *y* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="4efbc-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4efbc-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4efbc-105">Remarks</span></span>

<span data-ttu-id="4efbc-106">Wenn Sie einen Verweis auf die Zelle Y nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4efbc-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4efbc-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4efbc-107">Cell name:</span></span>  <br/> | <span data-ttu-id="4efbc-108">Connections.Y *i* wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4efbc-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4efbc-109">Wenn Sie einen Verweis auf die Zelle Y aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4efbc-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4efbc-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4efbc-110">Section index:</span></span>  <br/> |<span data-ttu-id="4efbc-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="4efbc-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="4efbc-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4efbc-112">Row index:</span></span>  <br/> |<span data-ttu-id="4efbc-113">**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4efbc-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4efbc-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4efbc-114">Cell index:</span></span>  <br/> |<span data-ttu-id="4efbc-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="4efbc-115">**visY**</span></span> <br/> |
   

