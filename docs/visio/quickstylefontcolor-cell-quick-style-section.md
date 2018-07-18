---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Bestimmt die Farbe der Schriftart aus dem Text einer Form des aktiven Designs, als ganze Zahl von 0 bis 1 erbt Schnellformatvorlagen-Satz.
ms.openlocfilehash: 8f2d77508dccffccf472f8ab80517e840f860541
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797755"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="91187-103">QuickStyleFontColor Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="91187-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="91187-104">Bestimmt die Farbe der Schriftart aus dem Text einer Form des aktiven Designs, als ganze Zahl von 0 bis 1 erbt Schnellformatvorlagen-Satz.</span><span class="sxs-lookup"><span data-stu-id="91187-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91187-105">Wert</span><span class="sxs-lookup"><span data-stu-id="91187-105">Value</span></span>  <br/> |<span data-ttu-id="91187-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91187-106">Description</span></span>  <br/> |
|<span data-ttu-id="91187-107">0</span><span class="sxs-lookup"><span data-stu-id="91187-107">0</span></span>  <br/> |<span data-ttu-id="91187-108">Der Shape-Text wird die dunklen Schriftfarbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="91187-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="91187-109">1</span><span class="sxs-lookup"><span data-stu-id="91187-109">1</span></span>  <br/> |<span data-ttu-id="91187-110">Der Shape-Text wird die helle Farbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="91187-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91187-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91187-111">Remarks</span></span>

<span data-ttu-id="91187-112">Wenn Sie einen Verweis auf die Zelle **QuickStyleFontColor** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="91187-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91187-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="91187-113">Cell name:</span></span>  <br/> | <span data-ttu-id="91187-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="91187-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="91187-115">Wenn Sie einen Verweis auf die Zelle **QuickStyleFontColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="91187-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91187-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="91187-116">Section index:</span></span>  <br/> |<span data-ttu-id="91187-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91187-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="91187-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="91187-118">Row index:</span></span>  <br/> |<span data-ttu-id="91187-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="91187-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="91187-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="91187-120">Cell index:</span></span>  <br/> |<span data-ttu-id="91187-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="91187-121">**visQuickStyleFontColor**</span></span> <br/> |
   

