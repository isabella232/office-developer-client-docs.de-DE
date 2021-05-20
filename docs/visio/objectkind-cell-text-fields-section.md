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
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438512"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="b7a93-103">Zelle "ObjectKind" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="b7a93-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="b7a93-104">Gibt den Textfeldtyp an.</span><span class="sxs-lookup"><span data-stu-id="b7a93-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="b7a93-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b7a93-105">**Value**</span></span>|<span data-ttu-id="b7a93-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7a93-106">**Description**</span></span>|<span data-ttu-id="b7a93-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b7a93-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b7a93-108">0</span><span class="sxs-lookup"><span data-stu-id="b7a93-108">0</span></span>  <br/> | <span data-ttu-id="b7a93-109">Standard</span><span class="sxs-lookup"><span data-stu-id="b7a93-109">Standard</span></span>  <br/> |<span data-ttu-id="b7a93-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="b7a93-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="b7a93-111">1</span><span class="sxs-lookup"><span data-stu-id="b7a93-111">1</span></span>  <br/> |<span data-ttu-id="b7a93-112">Horizontal in Vertikal</span><span class="sxs-lookup"><span data-stu-id="b7a93-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="b7a93-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="b7a93-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7a93-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7a93-114">Remarks</span></span>

<span data-ttu-id="b7a93-115">Die folgenden Typen von Textfeldern sind möglich:</span><span class="sxs-lookup"><span data-stu-id="b7a93-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="b7a93-116">Standard. Damit wird angegeben, dass das Feld nach Feldkategorie eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7a93-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="b7a93-117">Horizontal in Vertikal. Damit wird angegeben, dass im Feld horizontaler Text in vertikalen Text gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b7a93-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="b7a93-118">Um einen Verweis auf die Zelle ObjectKind anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b7a93-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7a93-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b7a93-119">Cell name:</span></span>  <br/> | <span data-ttu-id="b7a93-120">Fields.ObjectKind[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b7a93-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b7a93-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ObjectKind-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b7a93-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7a93-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b7a93-122">Section index:</span></span>  <br/> |<span data-ttu-id="b7a93-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b7a93-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="b7a93-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b7a93-124">Row index:</span></span>  <br/> |<span data-ttu-id="b7a93-125">**visRowField**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b7a93-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b7a93-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b7a93-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b7a93-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="b7a93-127">**visFieldObjectKind**</span></span> <br/> |
   

