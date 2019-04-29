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
description: Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap). In der Zelle ExtraInfo beispielsweise gibt x = 41&amp;y = die Koordinaten einer ImageMap 7specifies.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409573"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="3bc7e-104">Zelle "ExtraInfo" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="3bc7e-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="3bc7e-105">Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap).</span><span class="sxs-lookup"><span data-stu-id="3bc7e-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="3bc7e-106">In der Zelle ExtraInfo gibt beispielsweise "x = 41&amp;y = 7" die Koordinaten einer ImageMap an.</span><span class="sxs-lookup"><span data-stu-id="3bc7e-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3bc7e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bc7e-107">Remarks</span></span>

<span data-ttu-id="3bc7e-108">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="3bc7e-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="3bc7e-109">Wenn Sie einen Verweis auf die Zelle ExtraInfo aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3bc7e-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bc7e-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3bc7e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3bc7e-111">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="3bc7e-111">Hyperlink.</span></span>  <span data-ttu-id="3bc7e-112">*Name* . ExtraInfo, wobei Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="3bc7e-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="3bc7e-113">*Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="3bc7e-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="3bc7e-114">Wenn Sie einen Verweis auf die Zelle ExtraInfo aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3bc7e-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bc7e-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3bc7e-115">Section index:</span></span>  <br/> |<span data-ttu-id="3bc7e-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="3bc7e-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="3bc7e-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3bc7e-117">Row index:</span></span>  <br/> |<span data-ttu-id="3bc7e-118">**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3bc7e-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3bc7e-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3bc7e-119">Cell index:</span></span>  <br/> |<span data-ttu-id="3bc7e-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="3bc7e-120">**visHLinkExtraInfo**</span></span> <br/> |
   

