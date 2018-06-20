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
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798391"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="25e13-103">Zelle "VerticalAlign" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="25e13-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="25e13-104">Definiert die vertikale Ausrichtung von Text in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="25e13-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="25e13-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="25e13-105">**Value**</span></span>|<span data-ttu-id="25e13-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25e13-106">**Description**</span></span>|<span data-ttu-id="25e13-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="25e13-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="25e13-108">0</span><span class="sxs-lookup"><span data-stu-id="25e13-108">0</span></span>  <br/> | <span data-ttu-id="25e13-109">Oben</span><span class="sxs-lookup"><span data-stu-id="25e13-109">Top</span></span>  <br/> |<span data-ttu-id="25e13-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="25e13-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="25e13-111">1</span><span class="sxs-lookup"><span data-stu-id="25e13-111">1</span></span>  <br/> | <span data-ttu-id="25e13-112">Mitte</span><span class="sxs-lookup"><span data-stu-id="25e13-112">Middle</span></span>  <br/> |<span data-ttu-id="25e13-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="25e13-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="25e13-114">2</span><span class="sxs-lookup"><span data-stu-id="25e13-114">2</span></span>  <br/> | <span data-ttu-id="25e13-115">Unten</span><span class="sxs-lookup"><span data-stu-id="25e13-115">Bottom</span></span>  <br/> |<span data-ttu-id="25e13-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="25e13-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25e13-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25e13-117">Remarks</span></span>

<span data-ttu-id="25e13-118">Wenn Sie einen Verweis auf die Zelle VerticalAlign nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="25e13-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25e13-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="25e13-119">Cell name:</span></span>  <br/> | <span data-ttu-id="25e13-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="25e13-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="25e13-121">Wenn Sie einen Verweis auf die Zelle VerticalAlign aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="25e13-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25e13-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="25e13-122">Section index:</span></span>  <br/> |<span data-ttu-id="25e13-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="25e13-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="25e13-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="25e13-124">Row index:</span></span>  <br/> |<span data-ttu-id="25e13-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="25e13-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="25e13-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="25e13-126">Cell index:</span></span>  <br/> |<span data-ttu-id="25e13-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="25e13-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

