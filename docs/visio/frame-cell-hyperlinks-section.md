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
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344852"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="42073-104">Zelle "Frame" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="42073-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="42073-p102">Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="42073-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42073-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42073-107">Remarks</span></span>

<span data-ttu-id="42073-108">Wenn Sie einen Verweis auf die Zelle "Frame" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42073-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42073-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="42073-109">Cell name:</span></span>  <br/> | <span data-ttu-id="42073-110">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="42073-110">Hyperlink.</span></span>  <span data-ttu-id="42073-111">*Name* . Frame, auf dem Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="42073-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="42073-112">*Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="42073-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="42073-113">Wenn Sie einen Verweis auf die Zelle Rahmen aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="42073-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42073-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="42073-114">Section index:</span></span>  <br/> |<span data-ttu-id="42073-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="42073-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="42073-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="42073-116">Row index:</span></span>  <br/> |<span data-ttu-id="42073-117">**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="42073-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="42073-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="42073-118">Cell index:</span></span>  <br/> |<span data-ttu-id="42073-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="42073-119">**visHLinkFrame**</span></span> <br/> |
   

