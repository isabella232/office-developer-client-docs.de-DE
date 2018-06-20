---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Aufzählung des integrierten Microsoft Visio Design auf das Dokument, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt ist, wird die Zelle ThemeIndex für das Dokument und alle Seiten und Shapes darin enthaltenen mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798259"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="93d8d-104">ThemeIndex Cell (Theme Properties Section)</span><span class="sxs-lookup"><span data-stu-id="93d8d-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="93d8d-105">Speichert die Aufzählung des integrierten Microsoft Visio Design auf das Dokument, als ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="93d8d-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="93d8d-106">Wenn ein neues Design für das Dokument, das die Zelle **ThemeIndex** für das Dokument ausgewählt ist, und alle Seiten und die darin enthaltenen Shapes wird mit dem Index des integrierten Designs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="93d8d-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="93d8d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93d8d-107">Remarks</span></span>

<span data-ttu-id="93d8d-108">Wenn Sie einen Verweis auf die Zelle **ThemeIndex** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="93d8d-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93d8d-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="93d8d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="93d8d-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="93d8d-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="93d8d-111">Wenn Sie einen Verweis auf die Zelle **ThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="93d8d-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93d8d-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="93d8d-112">Section index:</span></span>  <br/> |<span data-ttu-id="93d8d-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="93d8d-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="93d8d-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="93d8d-114">Row index:</span></span>  <br/> |<span data-ttu-id="93d8d-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="93d8d-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="93d8d-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="93d8d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="93d8d-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="93d8d-117">**visThemeIndex**</span></span> <br/> |
   

