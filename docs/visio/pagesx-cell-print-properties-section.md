---
title: Zelle "PagesX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt horizontal dargestellt werden soll.
ms.openlocfilehash: 4f1cf3286e7b54dc90925bf2f1ab9fe8532022e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797596"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="d4576-103">PagesX Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="d4576-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="d4576-104">Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt horizontal dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4576-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d4576-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d4576-105">Remarks</span></span>

<span data-ttu-id="d4576-106">Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d4576-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="d4576-107">Wenn Sie einen Verweis auf die Zelle PagesX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d4576-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4576-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d4576-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d4576-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="d4576-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="d4576-110">Wenn Sie einen Verweis auf die Zelle PagesX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d4576-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4576-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d4576-111">Section index:</span></span>  <br/> |<span data-ttu-id="d4576-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4576-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d4576-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d4576-113">Row index:</span></span>  <br/> |<span data-ttu-id="d4576-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d4576-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d4576-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d4576-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d4576-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="d4576-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

