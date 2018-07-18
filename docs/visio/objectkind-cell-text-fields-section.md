---
title: Zelle "ObjectKind" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Gibt den Textfeldtyp an.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797552"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="b66c8-103">ObjectKind Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="b66c8-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="b66c8-104">Gibt den Textfeldtyp an.</span><span class="sxs-lookup"><span data-stu-id="b66c8-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="b66c8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b66c8-105">**Value**</span></span>|<span data-ttu-id="b66c8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b66c8-106">**Description**</span></span>|<span data-ttu-id="b66c8-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b66c8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b66c8-108">0</span><span class="sxs-lookup"><span data-stu-id="b66c8-108">0</span></span>  <br/> | <span data-ttu-id="b66c8-109">Standard</span><span class="sxs-lookup"><span data-stu-id="b66c8-109">Standard</span></span>  <br/> |<span data-ttu-id="b66c8-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="b66c8-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="b66c8-111">1</span><span class="sxs-lookup"><span data-stu-id="b66c8-111">1</span></span>  <br/> |<span data-ttu-id="b66c8-112">Horizontal in Vertikal</span><span class="sxs-lookup"><span data-stu-id="b66c8-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="b66c8-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="b66c8-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b66c8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b66c8-114">Remarks</span></span>

<span data-ttu-id="b66c8-115">Die folgenden Typen von Textfeldern sind möglich:</span><span class="sxs-lookup"><span data-stu-id="b66c8-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="b66c8-116">Standard. Damit wird angegeben, dass das Feld nach Feldkategorie eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b66c8-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="b66c8-117">Horizontal in Vertikal. Damit wird angegeben, dass im Feld horizontaler Text in vertikalen Text gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b66c8-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="b66c8-118">Wenn Sie einen Verweis auf die Zelle ObjectKind aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b66c8-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b66c8-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b66c8-119">Cell name:</span></span>  <br/> | <span data-ttu-id="b66c8-120">Fields.ObjectKind [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b66c8-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b66c8-121">Wenn Sie einen Verweis auf die Zelle ObjectKind aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b66c8-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b66c8-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b66c8-122">Section index:</span></span>  <br/> |<span data-ttu-id="b66c8-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b66c8-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="b66c8-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b66c8-124">Row index:</span></span>  <br/> |<span data-ttu-id="b66c8-125">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b66c8-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b66c8-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b66c8-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b66c8-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="b66c8-127">**visFieldObjectKind**</span></span> <br/> |
   

