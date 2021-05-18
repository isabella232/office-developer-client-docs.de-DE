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
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413885"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="d9adc-104">Zelle "OutputFormat" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="d9adc-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="d9adc-p102">Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.</span><span class="sxs-lookup"><span data-stu-id="d9adc-p102">Determines the output format for a drawing. Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="d9adc-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d9adc-107">**Value**</span></span>|<span data-ttu-id="d9adc-108">**Ausgabeformat**</span><span class="sxs-lookup"><span data-stu-id="d9adc-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d9adc-109">0</span><span class="sxs-lookup"><span data-stu-id="d9adc-109">0</span></span>  <br/> | <span data-ttu-id="d9adc-110">Drucken (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9adc-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="d9adc-111">1</span><span class="sxs-lookup"><span data-stu-id="d9adc-111">1</span></span>  <br/> | <span data-ttu-id="d9adc-112">PowerPoint-Präsentation</span><span class="sxs-lookup"><span data-stu-id="d9adc-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="d9adc-113">2</span><span class="sxs-lookup"><span data-stu-id="d9adc-113">2</span></span>  <br/> | <span data-ttu-id="d9adc-114">HTML- oder GIF-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d9adc-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9adc-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9adc-115">Remarks</span></span>

<span data-ttu-id="d9adc-116">Um einen Verweis auf die OutputFormat-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="d9adc-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d9adc-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d9adc-117">Cell name:</span></span>  <br/> | <span data-ttu-id="d9adc-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="d9adc-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="d9adc-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die OutputFormat-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d9adc-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d9adc-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d9adc-120">Section index:</span></span>  <br/> |<span data-ttu-id="d9adc-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d9adc-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d9adc-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d9adc-122">Row index:</span></span>  <br/> |<span data-ttu-id="d9adc-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="d9adc-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="d9adc-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d9adc-124">Cell index:</span></span>  <br/> |<span data-ttu-id="d9adc-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="d9adc-125">**visDocOutputFormat**</span></span> <br/> |
   

