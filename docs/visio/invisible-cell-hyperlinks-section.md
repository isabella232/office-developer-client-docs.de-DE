---
title: Zelle "Invisible" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404631"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="0294b-103">Zelle "Invisible" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="0294b-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="0294b-104">Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0294b-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="0294b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0294b-105">**Value**</span></span>|<span data-ttu-id="0294b-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0294b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0294b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0294b-107">TRUE</span></span>  <br/> |<span data-ttu-id="0294b-108">Im Kontextmenü wird kein Hyperlink als Menüelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0294b-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="0294b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0294b-109">FALSE</span></span>  <br/> |<span data-ttu-id="0294b-110">Im Kontextmenü wird ein Hyperlink als Menüelement angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="0294b-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0294b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0294b-111">Remarks</span></span>

<span data-ttu-id="0294b-112">Um einen Verweis auf die Zelle Invisible anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="0294b-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0294b-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0294b-113">Cell name:</span></span>  <br/> |<span data-ttu-id="0294b-114">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="0294b-114">Hyperlink.</span></span> <span data-ttu-id="0294b-115">*Name*  . Unsichtbar, wobei Hyperlink  *.name*  der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="0294b-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="0294b-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Invisible nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="0294b-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0294b-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0294b-117">Section index:</span></span>  <br/> |<span data-ttu-id="0294b-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="0294b-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="0294b-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0294b-119">Row index:</span></span>  <br/> |<span data-ttu-id="0294b-120">**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0294b-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0294b-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0294b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="0294b-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="0294b-122">**visHLinkInvisible**</span></span> <br/> |
   

