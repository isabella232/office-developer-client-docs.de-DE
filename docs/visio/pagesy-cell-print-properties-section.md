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
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339977"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="24563-103">Zelle "PagesY" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="24563-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="24563-104">Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="24563-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="24563-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24563-105">Remarks</span></span>

<span data-ttu-id="24563-106">Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="24563-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="24563-107">Wenn Sie einen Verweis auf die Zelle PagesY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="24563-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24563-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24563-108">Cell name:</span></span>  <br/> | <span data-ttu-id="24563-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="24563-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="24563-110">Wenn Sie einen Verweis auf die Zelle PagesY nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24563-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24563-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24563-111">Section index:</span></span>  <br/> |<span data-ttu-id="24563-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24563-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="24563-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24563-113">Row index:</span></span>  <br/> |<span data-ttu-id="24563-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="24563-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="24563-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24563-115">Cell index:</span></span>  <br/> |<span data-ttu-id="24563-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="24563-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

