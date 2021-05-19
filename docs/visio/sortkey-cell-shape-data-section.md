---
title: Zelle "SortKey" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417854"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="b66c6-103">Zelle "SortKey" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="b66c6-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="b66c6-104">Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster **Shape-Daten** aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="b66c6-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b66c6-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b66c6-105">Remarks</span></span>

<span data-ttu-id="b66c6-106">Die berechnung, die zum Vergleichen von SortKey-Werten verwendet wird, ist locale-specific und groß-/kleinschreibungsunempfindlich.</span><span class="sxs-lookup"><span data-stu-id="b66c6-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="b66c6-107">Wenn SortKey-Werte gleich sind, werden die Shapedaten in der Zeilenreihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b66c6-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="b66c6-108">Shapedaten ohne Sortierschlüssel werden nach Formdaten aufgelistet, die einen Sortierschlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="b66c6-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="b66c6-109">Nachfolgend finden Sie ein Beispiel für die Verwendung von Sortierschlüsseln, um die Shape-Daten im Fenster **Shape-Daten** in der folgenden Reihenfolge anzuzeigen: Artikelnummer, Menge, Preis.</span><span class="sxs-lookup"><span data-stu-id="b66c6-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="b66c6-110">*Row, Label und*  *SortKey*  beziehen sich auf Zellen in der Shape-Datenzeile.</span><span class="sxs-lookup"><span data-stu-id="b66c6-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="b66c6-111">In diesem Fall wurden diese Zeilen mit Shape-Daten mit einer Bezeichnung versehen.</span><span class="sxs-lookup"><span data-stu-id="b66c6-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="b66c6-112">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="b66c6-112">**Row**</span></span>|<span data-ttu-id="b66c6-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="b66c6-113">**Label**</span></span>|<span data-ttu-id="b66c6-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="b66c6-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b66c6-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="b66c6-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="b66c6-116">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="b66c6-116">Item Number</span></span>  <br/> | <span data-ttu-id="b66c6-117">1</span><span class="sxs-lookup"><span data-stu-id="b66c6-117">1</span></span>  <br/> |
| <span data-ttu-id="b66c6-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="b66c6-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="b66c6-119">Kurs</span><span class="sxs-lookup"><span data-stu-id="b66c6-119">Price</span></span>  <br/> | <span data-ttu-id="b66c6-120">3</span><span class="sxs-lookup"><span data-stu-id="b66c6-120">3</span></span>  <br/> |
| <span data-ttu-id="b66c6-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="b66c6-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="b66c6-122">Anzahl</span><span class="sxs-lookup"><span data-stu-id="b66c6-122">Quantity</span></span>  <br/> | <span data-ttu-id="b66c6-123">2</span><span class="sxs-lookup"><span data-stu-id="b66c6-123">2</span></span>  <br/> |
   
<span data-ttu-id="b66c6-124">Verwenden Sie zum Erhalten eines Verweises auf die Zelle SortKey anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="b66c6-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b66c6-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b66c6-125">Cell name:</span></span>  <br/> | <span data-ttu-id="b66c6-126">Prop.  *Name*  . SortKey, wobei Prop.  *Name*  ist der Name der benutzerdefinierten Eigenschaftenzeile</span><span class="sxs-lookup"><span data-stu-id="b66c6-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="b66c6-127">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SortKey nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b66c6-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b66c6-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b66c6-128">Section index:</span></span>  <br/> |<span data-ttu-id="b66c6-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="b66c6-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="b66c6-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b66c6-130">Row index:</span></span>  <br/> |<span data-ttu-id="b66c6-131">**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b66c6-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b66c6-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b66c6-132">Cell index:</span></span>  <br/> |<span data-ttu-id="b66c6-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="b66c6-133">**visCustPropsSortKey**</span></span> <br/> |
   

