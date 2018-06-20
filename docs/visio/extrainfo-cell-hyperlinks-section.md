---
title: Zelle "ExtraInfo" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Stellt eine Zeichenfolge, die Informationen für die Auflösung einer URL, beispielsweise die Koordinaten einer Imagemap übergibt. Beispielsweise in die Zelle ExtraInfo X = 41&amp;y = 7specifies die Koordinaten einer Imagemap.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796978"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="bf4b1-104">ExtraInfo Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="bf4b1-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="bf4b1-105">Stellt eine Zeichenfolge, die Informationen für die Auflösung einer URL, beispielsweise die Koordinaten einer Imagemap übergibt.</span><span class="sxs-lookup"><span data-stu-id="bf4b1-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="bf4b1-106">Beispielsweise in die Zelle ExtraInfo "X = 41&amp;y = 7" gibt die Koordinaten einer Imagemap an.</span><span class="sxs-lookup"><span data-stu-id="bf4b1-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf4b1-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf4b1-107">Remarks</span></span>

<span data-ttu-id="bf4b1-108">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="bf4b1-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="bf4b1-109">Wenn Sie einen Verweis auf die Zelle ExtraInfo nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf4b1-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf4b1-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bf4b1-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bf4b1-111">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="bf4b1-111">Hyperlink.</span></span>  <span data-ttu-id="bf4b1-112">*Name* . ExtraInfo, in dem Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="bf4b1-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="bf4b1-113">*Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="bf4b1-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="bf4b1-114">Wenn Sie einen Verweis auf die Zelle ExtraInfo aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bf4b1-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf4b1-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bf4b1-115">Section index:</span></span>  <br/> |<span data-ttu-id="bf4b1-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="bf4b1-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="bf4b1-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bf4b1-117">Row index:</span></span>  <br/> |<span data-ttu-id="bf4b1-118">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bf4b1-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bf4b1-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bf4b1-119">Cell index:</span></span>  <br/> |<span data-ttu-id="bf4b1-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="bf4b1-120">**visHLinkExtraInfo**</span></span> <br/> |
   

