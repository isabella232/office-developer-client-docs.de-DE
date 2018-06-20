---
title: Zelle "TxtWidth" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Definiert die Breite eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798346"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="c7a60-104">Zelle "TxtWidth" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="c7a60-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="c7a60-p102">Definiert die Breite eines Textblocks. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="c7a60-p102">Determines the width of the text block. The default formula is:</span></span>
  
<span data-ttu-id="c7a60-107">= Breite \* 1</span><span class="sxs-lookup"><span data-stu-id="c7a60-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7a60-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7a60-108">Remarks</span></span>

<span data-ttu-id="c7a60-109">Wenn Sie einen Verweis auf die Zelle TxtWidth nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c7a60-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7a60-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c7a60-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c7a60-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="c7a60-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="c7a60-112">Wenn Sie einen Verweis auf die Zelle TxtWidth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c7a60-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7a60-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c7a60-113">Section index:</span></span>  <br/> |<span data-ttu-id="c7a60-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7a60-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7a60-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c7a60-115">Row index:</span></span>  <br/> |<span data-ttu-id="c7a60-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="c7a60-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="c7a60-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c7a60-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c7a60-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="c7a60-118">**visXFormWidth**</span></span> <br/> |
   

