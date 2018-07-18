---
title: Zelle "Frame" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797076"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="9c33a-104">Frame Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="9c33a-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="9c33a-p102">Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9c33a-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c33a-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c33a-107">Remarks</span></span>

<span data-ttu-id="9c33a-108">Wenn Sie einen Verweis auf die Zelle Frame aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9c33a-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c33a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9c33a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9c33a-110">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="9c33a-110">Hyperlink.</span></span>  <span data-ttu-id="9c33a-111">*Name* . Where eingerahmt Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="9c33a-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="9c33a-112">*Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="9c33a-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9c33a-113">Wenn Sie einen Verweis auf die Zelle Frame aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9c33a-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c33a-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9c33a-114">Section index:</span></span>  <br/> |<span data-ttu-id="9c33a-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="9c33a-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="9c33a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9c33a-116">Row index:</span></span>  <br/> |<span data-ttu-id="9c33a-117">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9c33a-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9c33a-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9c33a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9c33a-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="9c33a-119">**visHLinkFrame**</span></span> <br/> |
   

