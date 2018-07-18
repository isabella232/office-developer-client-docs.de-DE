---
title: Zelle "SortKey" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798170"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="9e3cd-103">SortKey Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="9e3cd-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="9e3cd-104">Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e3cd-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e3cd-105">Remarks</span></span>

<span data-ttu-id="9e3cd-p101">Die Hyperlinks in Kontextmenüs werden von unten nach oben sortiert, wobei die Hyperlinks mit der kleinsten Nummer im Menü an oberster Stelle angezeigt werden. Wenn zwei Hyperlinks für die Zelle SortKey denselben Wert aufweisen, wird die Reihenfolge durch die physische Zeilenreihenfolge bestimmt. Der Standardwert ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="9e3cd-p101">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span> 
  
<span data-ttu-id="9e3cd-109">Wenn Sie einen Verweis auf die Zelle SortKey aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e3cd-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-110">Cell name:</span></span>  <br/> |<span data-ttu-id="9e3cd-111">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-111">Hyperlink.</span></span> <span data-ttu-id="9e3cd-112">*Name* . SortKey, in dem Hyperlink *.name* der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="9e3cd-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9e3cd-113">Wenn Sie einen Verweis auf die Zelle SortKey aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e3cd-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-114">Section index:</span></span>  <br/> |<span data-ttu-id="9e3cd-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="9e3cd-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="9e3cd-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-116">Row index:</span></span>  <br/> |<span data-ttu-id="9e3cd-117">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9e3cd-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9e3cd-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9e3cd-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="9e3cd-119">**visHLinkSortKey**</span></span> <br/> |
   

