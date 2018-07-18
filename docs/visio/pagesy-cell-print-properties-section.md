---
title: Zelle "PagesY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll.
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797589"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="1611b-103">PagesY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="1611b-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="1611b-104">Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1611b-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1611b-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1611b-105">Remarks</span></span>

<span data-ttu-id="1611b-106">Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1611b-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="1611b-107">Wenn Sie einen Verweis auf die Zelle PagesY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1611b-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1611b-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1611b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="1611b-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="1611b-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="1611b-110">Wenn Sie einen Verweis auf die Zelle PagesY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1611b-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1611b-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1611b-111">Section index:</span></span>  <br/> |<span data-ttu-id="1611b-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1611b-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1611b-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1611b-113">Row index:</span></span>  <br/> |<span data-ttu-id="1611b-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="1611b-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="1611b-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1611b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="1611b-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="1611b-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

