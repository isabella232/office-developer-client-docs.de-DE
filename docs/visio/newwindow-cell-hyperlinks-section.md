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
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342231"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="b50df-103">Zelle "NewWindow" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="b50df-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="b50df-104">Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b50df-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="b50df-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b50df-105">**Value**</span></span>|<span data-ttu-id="b50df-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b50df-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b50df-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b50df-107">TRUE</span></span>  <br/> | <span data-ttu-id="b50df-108">Öffnen Sie die verknüpfte Seite, das Dokument oder die Website in einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="b50df-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="b50df-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b50df-109">FALSE</span></span>  <br/> | <span data-ttu-id="b50df-p101">Standard. Hyperlink nicht in einem neuen Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="b50df-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b50df-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b50df-112">Remarks</span></span>

<span data-ttu-id="b50df-113">Um einen Verweis auf die Zelle NewWindow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b50df-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b50df-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b50df-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b50df-115">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="b50df-115">Hyperlink.</span></span>  <span data-ttu-id="b50df-116">*Name*  . NewWindow, wobei Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="b50df-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="b50df-117">*Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="b50df-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b50df-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NewWindow-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b50df-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b50df-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b50df-119">Section index:</span></span>  <br/> |<span data-ttu-id="b50df-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b50df-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="b50df-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b50df-121">Row index:</span></span>  <br/> |<span data-ttu-id="b50df-122">**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="b50df-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="b50df-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b50df-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b50df-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="b50df-124">**visHLinkNewWin**</span></span> <br/> |
   

