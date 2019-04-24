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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356141"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="c9ffc-103">Zelle "VerticalAlign" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="c9ffc-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="c9ffc-104">Definiert die vertikale Ausrichtung von Text in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="c9ffc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-105">**Value**</span></span>|<span data-ttu-id="c9ffc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-106">**Description**</span></span>|<span data-ttu-id="c9ffc-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c9ffc-108">0</span><span class="sxs-lookup"><span data-stu-id="c9ffc-108">0</span></span>  <br/> | <span data-ttu-id="c9ffc-109">Oben</span><span class="sxs-lookup"><span data-stu-id="c9ffc-109">Top</span></span>  <br/> |<span data-ttu-id="c9ffc-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="c9ffc-111">1</span><span class="sxs-lookup"><span data-stu-id="c9ffc-111">1</span></span>  <br/> | <span data-ttu-id="c9ffc-112">Mittleren</span><span class="sxs-lookup"><span data-stu-id="c9ffc-112">Middle</span></span>  <br/> |<span data-ttu-id="c9ffc-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="c9ffc-114">2</span><span class="sxs-lookup"><span data-stu-id="c9ffc-114">2</span></span>  <br/> | <span data-ttu-id="c9ffc-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="c9ffc-115">Bottom</span></span>  <br/> |<span data-ttu-id="c9ffc-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9ffc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9ffc-117">Remarks</span></span>

<span data-ttu-id="c9ffc-118">Wenn Sie einen Verweis auf die Zelle VerticalAlign aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9ffc-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-119">Cell name:</span></span>  <br/> | <span data-ttu-id="c9ffc-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="c9ffc-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="c9ffc-121">Wenn Sie einen Verweis auf die Zelle VerticalAlign aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9ffc-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-122">Section index:</span></span>  <br/> |<span data-ttu-id="c9ffc-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c9ffc-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-124">Row index:</span></span>  <br/> |<span data-ttu-id="c9ffc-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="c9ffc-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-126">Cell index:</span></span>  <br/> |<span data-ttu-id="c9ffc-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

