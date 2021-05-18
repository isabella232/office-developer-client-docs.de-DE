---
title: Zelle "Y" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Represents the y -coordinate that indicates the location of a shape's control handle in local coordinates.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407949"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="7e168-103">Zelle "Y" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="7e168-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="7e168-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span><span class="sxs-lookup"><span data-stu-id="7e168-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e168-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e168-105">Remarks</span></span>

<span data-ttu-id="7e168-106">Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="7e168-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e168-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7e168-107">Cell name:</span></span>  <br/> | <span data-ttu-id="7e168-108">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="7e168-108">Controls.</span></span>  <span data-ttu-id="7e168-109">*Name*  . Ywhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="7e168-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="7e168-110">*name*  ist der Name der Steuerelementzeile.</span><span class="sxs-lookup"><span data-stu-id="7e168-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="7e168-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="7e168-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e168-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7e168-112">Section index:</span></span>  <br/> |<span data-ttu-id="7e168-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="7e168-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="7e168-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7e168-114">Row index:</span></span>  <br/> |<span data-ttu-id="7e168-115">**visRowControl**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7e168-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7e168-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7e168-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7e168-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="7e168-117">**visCtlY**</span></span> <br/> |
   

