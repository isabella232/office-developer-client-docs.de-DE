---
title: Zelle "VerticalAlign" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Definiert die vertikale Ausrichtung von Text in einem Textblock.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425792"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="a74b9-103">Zelle "VerticalAlign" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="a74b9-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="a74b9-104">Definiert die vertikale Ausrichtung von Text in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="a74b9-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="a74b9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a74b9-105">**Value**</span></span>|<span data-ttu-id="a74b9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a74b9-106">**Description**</span></span>|<span data-ttu-id="a74b9-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="a74b9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a74b9-108">0</span><span class="sxs-lookup"><span data-stu-id="a74b9-108">0</span></span>  <br/> | <span data-ttu-id="a74b9-109">Oben</span><span class="sxs-lookup"><span data-stu-id="a74b9-109">Top</span></span>  <br/> |<span data-ttu-id="a74b9-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="a74b9-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="a74b9-111">1</span><span class="sxs-lookup"><span data-stu-id="a74b9-111">1</span></span>  <br/> | <span data-ttu-id="a74b9-112">Middle</span><span class="sxs-lookup"><span data-stu-id="a74b9-112">Middle</span></span>  <br/> |<span data-ttu-id="a74b9-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="a74b9-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="a74b9-114">2</span><span class="sxs-lookup"><span data-stu-id="a74b9-114">2</span></span>  <br/> | <span data-ttu-id="a74b9-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="a74b9-115">Bottom</span></span>  <br/> |<span data-ttu-id="a74b9-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="a74b9-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a74b9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a74b9-117">Remarks</span></span>

<span data-ttu-id="a74b9-118">Verwenden Sie zum Erhalten eines Verweises auf die Zelle VerticalAlign anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="a74b9-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a74b9-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a74b9-119">Cell name:</span></span>  <br/> | <span data-ttu-id="a74b9-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="a74b9-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="a74b9-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die VerticalAlign-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="a74b9-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a74b9-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a74b9-122">Section index:</span></span>  <br/> |<span data-ttu-id="a74b9-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a74b9-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a74b9-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a74b9-124">Row index:</span></span>  <br/> |<span data-ttu-id="a74b9-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="a74b9-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="a74b9-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a74b9-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a74b9-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="a74b9-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

