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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360991"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="9f690-103">Zelle "ObjectKind" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="9f690-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="9f690-104">Gibt den Textfeldtyp an.</span><span class="sxs-lookup"><span data-stu-id="9f690-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="9f690-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9f690-105">**Value**</span></span>|<span data-ttu-id="9f690-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f690-106">**Description**</span></span>|<span data-ttu-id="9f690-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9f690-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9f690-108">0</span><span class="sxs-lookup"><span data-stu-id="9f690-108">0</span></span>  <br/> | <span data-ttu-id="9f690-109">Standard</span><span class="sxs-lookup"><span data-stu-id="9f690-109">Standard</span></span>  <br/> |<span data-ttu-id="9f690-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="9f690-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="9f690-111">1</span><span class="sxs-lookup"><span data-stu-id="9f690-111">1</span></span>  <br/> |<span data-ttu-id="9f690-112">Horizontal in Vertikal</span><span class="sxs-lookup"><span data-stu-id="9f690-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="9f690-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="9f690-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f690-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f690-114">Remarks</span></span>

<span data-ttu-id="9f690-115">Die folgenden Typen von Textfeldern sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9f690-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="9f690-116">Standard. Damit wird angegeben, dass das Feld nach Feldkategorie eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="9f690-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="9f690-117">Horizontal in Vertikal. Damit wird angegeben, dass im Feld horizontaler Text in vertikalen Text gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="9f690-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="9f690-118">Wenn Sie einen Verweis auf die Zelle objectKind aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9f690-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f690-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9f690-119">Cell name:</span></span>  <br/> | <span data-ttu-id="9f690-120">Fields. objectKind [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9f690-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9f690-121">Wenn Sie einen Verweis auf die Zelle objectKind aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9f690-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f690-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9f690-122">Section index:</span></span>  <br/> |<span data-ttu-id="9f690-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="9f690-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="9f690-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9f690-124">Row index:</span></span>  <br/> |<span data-ttu-id="9f690-125">**visRowField** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9f690-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9f690-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9f690-126">Cell index:</span></span>  <br/> |<span data-ttu-id="9f690-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="9f690-127">**visFieldObjectKind**</span></span> <br/> |
   

