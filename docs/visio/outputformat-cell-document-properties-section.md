---
title: Zelle "OutputFormat" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797567"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="78e6e-104">OutputFormat Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="78e6e-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="78e6e-p102">Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.</span><span class="sxs-lookup"><span data-stu-id="78e6e-p102">Determines the output format for a drawing. Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="78e6e-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="78e6e-107">**Value**</span></span>|<span data-ttu-id="78e6e-108">**OutputFormat**</span><span class="sxs-lookup"><span data-stu-id="78e6e-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="78e6e-109">0</span><span class="sxs-lookup"><span data-stu-id="78e6e-109">0</span></span>  <br/> | <span data-ttu-id="78e6e-110">Drucken (Standard)</span><span class="sxs-lookup"><span data-stu-id="78e6e-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="78e6e-111">1</span><span class="sxs-lookup"><span data-stu-id="78e6e-111">1</span></span>  <br/> | <span data-ttu-id="78e6e-112">PowerPoint-Präsentation</span><span class="sxs-lookup"><span data-stu-id="78e6e-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="78e6e-113">2</span><span class="sxs-lookup"><span data-stu-id="78e6e-113">2</span></span>  <br/> | <span data-ttu-id="78e6e-114">HTML- oder GIF-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="78e6e-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78e6e-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78e6e-115">Remarks</span></span>

<span data-ttu-id="78e6e-116">Wenn Sie einen Verweis auf die Zelle OutputFormat aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="78e6e-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="78e6e-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="78e6e-117">Cell name:</span></span>  <br/> | <span data-ttu-id="78e6e-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="78e6e-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="78e6e-119">Wenn Sie einen Verweis auf die Zelle OutputFormat aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="78e6e-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="78e6e-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="78e6e-120">Section index:</span></span>  <br/> |<span data-ttu-id="78e6e-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="78e6e-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="78e6e-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="78e6e-122">Row index:</span></span>  <br/> |<span data-ttu-id="78e6e-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="78e6e-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="78e6e-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="78e6e-124">Cell index:</span></span>  <br/> |<span data-ttu-id="78e6e-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="78e6e-125">**visDocOutputFormat**</span></span> <br/> |
   

