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
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405674"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="29357-103">Zelle "LocalizeMerge" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="29357-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="29357-104">Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="29357-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="29357-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="29357-105">**Value**</span></span>|<span data-ttu-id="29357-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29357-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="29357-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="29357-107">TRUE</span></span>  <br/> | <span data-ttu-id="29357-108">Shapes werden in die Sprache des Zieldokuments lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="29357-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="29357-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="29357-109">FALSE</span></span>  <br/> | <span data-ttu-id="29357-110">Ein Shape kann nicht basierend auf der Sprache des Zieldokuments lokalisiert werden (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="29357-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29357-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29357-111">Remarks</span></span>

<span data-ttu-id="29357-112">Wenn Sie einen Verweis auf die Zelle Zelle LocalizeMerge aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="29357-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29357-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="29357-113">Cell name:</span></span>  <br/> | <span data-ttu-id="29357-114">Zelle LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="29357-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="29357-115">Wenn Sie einen Verweis auf die Zelle Zelle LocalizeMerge aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="29357-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29357-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="29357-116">Section index:</span></span>  <br/> |<span data-ttu-id="29357-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29357-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="29357-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="29357-118">Row index:</span></span>  <br/> |<span data-ttu-id="29357-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="29357-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="29357-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="29357-120">Cell index:</span></span>  <br/> |<span data-ttu-id="29357-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="29357-121">**visObjLocalizeMerge**</span></span> <br/> |
   

