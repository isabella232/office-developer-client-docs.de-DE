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
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340138"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="7bec8-103">Zelle "PagesX" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="7bec8-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="7bec8-104">Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt horizontal dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bec8-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7bec8-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bec8-105">Remarks</span></span>

<span data-ttu-id="7bec8-106">Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7bec8-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="7bec8-107">Wenn Sie einen Verweis auf die Zelle PagesX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7bec8-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7bec8-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7bec8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="7bec8-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="7bec8-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="7bec8-110">Wenn Sie einen Verweis auf die Zelle PagesX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7bec8-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7bec8-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7bec8-111">Section index:</span></span>  <br/> |<span data-ttu-id="7bec8-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7bec8-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7bec8-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7bec8-113">Row index:</span></span>  <br/> |<span data-ttu-id="7bec8-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="7bec8-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="7bec8-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7bec8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="7bec8-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="7bec8-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

