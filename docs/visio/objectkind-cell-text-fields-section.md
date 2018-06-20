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
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="6dbed-103">Zelle "ObjectKind" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="6dbed-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="6dbed-104">Gibt den Textfeldtyp an.</span><span class="sxs-lookup"><span data-stu-id="6dbed-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="6dbed-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6dbed-105">**Value**</span></span>|<span data-ttu-id="6dbed-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6dbed-106">**Description**</span></span>|<span data-ttu-id="6dbed-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="6dbed-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6dbed-108">0</span><span class="sxs-lookup"><span data-stu-id="6dbed-108">0</span></span>  <br/> | <span data-ttu-id="6dbed-109">Standard</span><span class="sxs-lookup"><span data-stu-id="6dbed-109">Standard</span></span>  <br/> |<span data-ttu-id="6dbed-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="6dbed-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="6dbed-111">1</span><span class="sxs-lookup"><span data-stu-id="6dbed-111">1</span></span>  <br/> |<span data-ttu-id="6dbed-112">Horizontal in Vertikal</span><span class="sxs-lookup"><span data-stu-id="6dbed-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="6dbed-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="6dbed-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dbed-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6dbed-114">Remarks</span></span>

<span data-ttu-id="6dbed-115">Die folgenden Typen von Textfeldern sind möglich:</span><span class="sxs-lookup"><span data-stu-id="6dbed-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="6dbed-116">Standard. Damit wird angegeben, dass das Feld nach Feldkategorie eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6dbed-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="6dbed-117">Horizontal in Vertikal. Damit wird angegeben, dass im Feld horizontaler Text in vertikalen Text gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="6dbed-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="6dbed-118">Wenn Sie einen Verweis auf die Zelle ObjectKind nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6dbed-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6dbed-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6dbed-119">Cell name:</span></span>  <br/> | <span data-ttu-id="6dbed-120">Fields.ObjectKind [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6dbed-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6dbed-121">Wenn Sie einen Verweis auf die Zelle ObjectKind aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6dbed-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6dbed-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6dbed-122">Section index:</span></span>  <br/> |<span data-ttu-id="6dbed-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="6dbed-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="6dbed-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6dbed-124">Row index:</span></span>  <br/> |<span data-ttu-id="6dbed-125">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6dbed-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6dbed-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6dbed-126">Cell index:</span></span>  <br/> |<span data-ttu-id="6dbed-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="6dbed-127">**visFieldObjectKind**</span></span> <br/> |
   

