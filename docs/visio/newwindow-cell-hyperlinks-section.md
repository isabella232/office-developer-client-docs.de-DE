---
title: Zelle "NewWindow" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797542"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="748d3-103">NewWindow Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="748d3-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="748d3-104">Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="748d3-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="748d3-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="748d3-105">**Value**</span></span>|<span data-ttu-id="748d3-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="748d3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="748d3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="748d3-107">TRUE</span></span>  <br/> | <span data-ttu-id="748d3-108">Verknüpfte Seite, Dokument oder Website in einem neuen Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="748d3-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="748d3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="748d3-109">FALSE</span></span>  <br/> | <span data-ttu-id="748d3-p101">Standard. Hyperlink nicht in einem neuen Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="748d3-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="748d3-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="748d3-112">Remarks</span></span>

<span data-ttu-id="748d3-113">Wenn Sie einen Verweis auf die Zelle NewWindow nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="748d3-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="748d3-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="748d3-114">Cell name:</span></span>  <br/> | <span data-ttu-id="748d3-115">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="748d3-115">Hyperlink.</span></span>  <span data-ttu-id="748d3-116">*Name* . NewWindow, in dem Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="748d3-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="748d3-117">*Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="748d3-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="748d3-118">Wenn Sie einen Verweis auf die Zelle NewWindow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="748d3-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="748d3-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="748d3-119">Section index:</span></span>  <br/> |<span data-ttu-id="748d3-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="748d3-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="748d3-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="748d3-121">Row index:</span></span>  <br/> |<span data-ttu-id="748d3-122">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="748d3-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="748d3-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="748d3-123">Cell index:</span></span>  <br/> |<span data-ttu-id="748d3-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="748d3-124">**visHLinkNewWin**</span></span> <br/> |
   

