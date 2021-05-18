---
title: Zelle "DefaultTabstop" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Bestimmt das Intervall der Standardtabstopps in einem Textblock.
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407830"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="13ec6-103">Zelle "DefaultTabstop" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="13ec6-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="13ec6-104">Bestimmt das Intervall der Standardtabstopps in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="13ec6-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="13ec6-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13ec6-105">Remarks</span></span>

<span data-ttu-id="13ec6-106">Der Standardwert ist 1,27 cm für Dokumente, die unter Verwendung britischer Maßeinheiten erstellt wurden, oder 1,5 cm für Dokumente, die in metrischen Maßeinheiten erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="13ec6-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="13ec6-107">Um einen Verweis auf die Zelle DefaultTabstop anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="13ec6-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13ec6-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="13ec6-108">Cell name:</span></span>  <br/> |<span data-ttu-id="13ec6-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="13ec6-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="13ec6-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DefaultTabstop-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="13ec6-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13ec6-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="13ec6-111">Section index:</span></span>  <br/> |<span data-ttu-id="13ec6-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="13ec6-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="13ec6-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="13ec6-113">Row index:</span></span>  <br/> |<span data-ttu-id="13ec6-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="13ec6-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="13ec6-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="13ec6-115">Cell index:</span></span>  <br/> |<span data-ttu-id="13ec6-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="13ec6-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

