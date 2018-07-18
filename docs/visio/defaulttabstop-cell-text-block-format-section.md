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
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796837"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="a6809-103">DefaultTabstop Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="a6809-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="a6809-104">Bestimmt das Intervall der Standardtabstopps in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="a6809-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6809-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6809-105">Remarks</span></span>

<span data-ttu-id="a6809-106">Der Standardwert ist 1,27 cm für Dokumente, die unter Verwendung britischer Maßeinheiten erstellt wurden, oder 1,5 cm für Dokumente, die in metrischen Maßeinheiten erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a6809-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="a6809-107">Wenn Sie einen Verweis auf die Zelle DefaultTabstop aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6809-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6809-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a6809-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a6809-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="a6809-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="a6809-110">Wenn Sie einen Verweis auf die Zelle DefaultTabstop aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a6809-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6809-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a6809-111">Section index:</span></span>  <br/> |<span data-ttu-id="a6809-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6809-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a6809-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a6809-113">Row index:</span></span>  <br/> |<span data-ttu-id="a6809-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="a6809-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="a6809-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a6809-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a6809-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="a6809-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

