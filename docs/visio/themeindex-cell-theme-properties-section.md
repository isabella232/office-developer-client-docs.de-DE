---
title: ThemeIndex Cell (Theme Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Enumeration des integrierten Microsoft Visio-Designs, das auf das Dokument angewendet wird, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die ThemeIndex-Zelle für das Dokument und alle darin enthaltenen Seiten und Formen mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411911"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="34317-104">ThemeIndex Cell (Theme Properties section)</span><span class="sxs-lookup"><span data-stu-id="34317-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="34317-105">Speichert die Enumeration des integrierten Microsoft Visio-Designs, das auf das Dokument angewendet wird, als ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="34317-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="34317-106">Wenn ein neues Design für das Dokument ausgewählt wird, wird die **ThemeIndex** -Zelle für das Dokument und alle darin enthaltenen Seiten und Formen mit dem Index des integrierten Designs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="34317-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="34317-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34317-107">Remarks</span></span>

<span data-ttu-id="34317-108">Wenn Sie einen Verweis auf die Zelle **ThemeIndex** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="34317-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34317-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="34317-109">Cell name:</span></span>  <br/> | <span data-ttu-id="34317-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="34317-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="34317-111">Wenn Sie einen Verweis auf die Zelle **ThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="34317-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34317-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="34317-112">Section index:</span></span>  <br/> |<span data-ttu-id="34317-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34317-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="34317-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="34317-114">Row index:</span></span>  <br/> |<span data-ttu-id="34317-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="34317-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="34317-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="34317-116">Cell index:</span></span>  <br/> |<span data-ttu-id="34317-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="34317-117">**visThemeIndex**</span></span> <br/> |
   

