---
title: Zelle "LocalizeMerge" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797353"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="e9ca8-103">LocalizeMerge Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="e9ca8-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="e9ca8-104">Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="e9ca8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e9ca8-105">**Value**</span></span>|<span data-ttu-id="e9ca8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9ca8-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e9ca8-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="e9ca8-107">TRUE</span></span>  <br/> | <span data-ttu-id="e9ca8-108">Shapes werden in die Sprache des Zieldokuments lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="e9ca8-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="e9ca8-109">FALSE</span></span>  <br/> | <span data-ttu-id="e9ca8-110">Ein Shape auf Grundlage der Sprache des Zieldokuments (Standard) nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9ca8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9ca8-111">Remarks</span></span>

<span data-ttu-id="e9ca8-112">Wenn Sie einen Verweis auf die Zelle LocalizeMerge nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9ca8-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e9ca8-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="e9ca8-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="e9ca8-115">Wenn Sie einen Verweis auf die Zelle LocalizeMerge aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9ca8-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-116">Section index:</span></span>  <br/> |<span data-ttu-id="e9ca8-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9ca8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e9ca8-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-118">Row index:</span></span>  <br/> |<span data-ttu-id="e9ca8-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="e9ca8-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="e9ca8-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e9ca8-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="e9ca8-121">**visObjLocalizeMerge**</span></span> <br/> |
   

