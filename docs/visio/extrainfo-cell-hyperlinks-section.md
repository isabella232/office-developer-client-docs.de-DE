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
description: Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap). Beispielsweise werden in der Zelle ExtraInfo x=41 &amp; y=7 die Koordinaten einer Bildzuordnung angegeben.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409573"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="ecf6b-104">Zelle "ExtraInfo" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="ecf6b-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="ecf6b-105">Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap).</span><span class="sxs-lookup"><span data-stu-id="ecf6b-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="ecf6b-106">Beispielsweise gibt "x=41 y=7" in der Zelle ExtraInfo die Koordinaten einer &amp; Bildzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="ecf6b-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ecf6b-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ecf6b-107">Remarks</span></span>

<span data-ttu-id="ecf6b-108">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="ecf6b-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="ecf6b-109">Verwenden Sie zum Abrufen eines Verweises auf die Zelle ExtraInfo anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="ecf6b-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecf6b-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ecf6b-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ecf6b-111">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="ecf6b-111">Hyperlink.</span></span>  <span data-ttu-id="ecf6b-112">*Name*  . ExtraInfo, wobei Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="ecf6b-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="ecf6b-113">*Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="ecf6b-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="ecf6b-114">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ExtraInfo-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ecf6b-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecf6b-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ecf6b-115">Section index:</span></span>  <br/> |<span data-ttu-id="ecf6b-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="ecf6b-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="ecf6b-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ecf6b-117">Row index:</span></span>  <br/> |<span data-ttu-id="ecf6b-118">**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ecf6b-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ecf6b-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ecf6b-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ecf6b-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="ecf6b-120">**visHLinkExtraInfo**</span></span> <br/> |
   

