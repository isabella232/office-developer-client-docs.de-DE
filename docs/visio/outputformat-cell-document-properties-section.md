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
description: Bestimmt das Ausgabeformat für eine Zeichnung. Zeichnungs Seiten sind normalerweise zum Drucken formatiert (Standard); Sie können jedoch auch andere Ausgabeformate auswählen.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413885"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="5f3f2-104">Zelle "OutputFormat" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="5f3f2-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="5f3f2-105">Bestimmt das Ausgabeformat für eine Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="5f3f2-105">Determines the output format for a drawing.</span></span> <span data-ttu-id="5f3f2-106">Zeichnungs Seiten sind normalerweise zum Drucken formatiert (Standard); Sie können jedoch auch andere Ausgabeformate auswählen.</span><span class="sxs-lookup"><span data-stu-id="5f3f2-106">Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="5f3f2-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5f3f2-107">**Value**</span></span>|<span data-ttu-id="5f3f2-108">**Ausgabeformat**</span><span class="sxs-lookup"><span data-stu-id="5f3f2-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5f3f2-109">0</span><span class="sxs-lookup"><span data-stu-id="5f3f2-109">0</span></span>  <br/> | <span data-ttu-id="5f3f2-110">Drucken (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f3f2-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="5f3f2-111">1</span><span class="sxs-lookup"><span data-stu-id="5f3f2-111">1</span></span>  <br/> | <span data-ttu-id="5f3f2-112">PowerPoint-Präsentation</span><span class="sxs-lookup"><span data-stu-id="5f3f2-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="5f3f2-113">2</span><span class="sxs-lookup"><span data-stu-id="5f3f2-113">2</span></span>  <br/> | <span data-ttu-id="5f3f2-114">HTML- oder GIF-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5f3f2-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f3f2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f3f2-115">Remarks</span></span>

<span data-ttu-id="5f3f2-116">Wenn Sie einen Verweis auf die Zelle OutputFormat aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5f3f2-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f3f2-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5f3f2-117">Cell name:</span></span>  <br/> | <span data-ttu-id="5f3f2-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="5f3f2-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="5f3f2-119">Wenn Sie einen Verweis auf die Zelle OutputFormat aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5f3f2-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f3f2-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5f3f2-120">Section index:</span></span>  <br/> |<span data-ttu-id="5f3f2-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5f3f2-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5f3f2-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5f3f2-122">Row index:</span></span>  <br/> |<span data-ttu-id="5f3f2-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="5f3f2-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="5f3f2-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5f3f2-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5f3f2-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="5f3f2-125">**visDocOutputFormat**</span></span> <br/> |
   

