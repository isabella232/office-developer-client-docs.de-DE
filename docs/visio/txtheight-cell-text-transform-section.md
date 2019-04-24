---
title: Zelle "TxtHeight" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Definiert die Höhe eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334391"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="61a51-104">Zelle "TxtHeight" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="61a51-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="61a51-105">Definiert die Höhe eines Textblocks.</span><span class="sxs-lookup"><span data-stu-id="61a51-105">Determines the height of the text block.</span></span> <span data-ttu-id="61a51-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="61a51-106">The default formula is:</span></span>
  
<span data-ttu-id="61a51-107">= Höhe \* 1</span><span class="sxs-lookup"><span data-stu-id="61a51-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61a51-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61a51-108">Remarks</span></span>

<span data-ttu-id="61a51-109">Wenn Sie einen Verweis auf die Zelle Zelle TxtHeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="61a51-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61a51-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="61a51-110">Cell name:</span></span>  <br/> | <span data-ttu-id="61a51-111">Zelle TxtHeight</span><span class="sxs-lookup"><span data-stu-id="61a51-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="61a51-112">Wenn Sie einen Verweis auf die Zelle Zelle TxtHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="61a51-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61a51-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="61a51-113">Section index:</span></span>  <br/> |<span data-ttu-id="61a51-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61a51-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="61a51-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="61a51-115">Row index:</span></span>  <br/> |<span data-ttu-id="61a51-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="61a51-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="61a51-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="61a51-117">Cell index:</span></span>  <br/> |<span data-ttu-id="61a51-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="61a51-118">**visXFormHeight**</span></span> <br/> |
   

