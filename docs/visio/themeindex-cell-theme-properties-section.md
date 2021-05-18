---
title: Zelle "ThemeIndex" (Abschnitt "Theme Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Aufzählung des integrierten Microsoft Visio, das auf das Dokument angewendet wurde, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die Zelle ThemeIndex für das Dokument und alle seiten und Formen, die es enthält, mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411911"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="1dcaa-104">Zelle "ThemeIndex" (Abschnitt "Theme Properties")</span><span class="sxs-lookup"><span data-stu-id="1dcaa-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="1dcaa-105">Speichert die Aufzählung des integrierten Microsoft Visio, das auf das Dokument angewendet wurde, als ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="1dcaa-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="1dcaa-106">Wenn ein neues Design für das Dokument ausgewählt wird, wird die **Zelle ThemeIndex** für das Dokument und alle seiten und Formen, die es enthält, mit dem Index des integrierten Designs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1dcaa-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1dcaa-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1dcaa-107">Remarks</span></span>

<span data-ttu-id="1dcaa-108">Verwenden Sie zum Erhalten eines Verweises auf die **ThemeIndex-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="1dcaa-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dcaa-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1dcaa-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1dcaa-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="1dcaa-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="1dcaa-111">Um einen Verweis auf die **ThemeIndex-Zelle** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1dcaa-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dcaa-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1dcaa-112">Section index:</span></span>  <br/> |<span data-ttu-id="1dcaa-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1dcaa-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1dcaa-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1dcaa-114">Row index:</span></span>  <br/> |<span data-ttu-id="1dcaa-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="1dcaa-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="1dcaa-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1dcaa-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1dcaa-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="1dcaa-117">**visThemeIndex**</span></span> <br/> |
   

