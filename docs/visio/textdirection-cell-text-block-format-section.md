---
title: Zelle "TextDirection" (Abschnitt "Text Block Format ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Bestimmt die Richtung der Zeichen in einem Textblock.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406227"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="ed593-103">Zelle "TextDirection" (Abschnitt "Text Block Format ")</span><span class="sxs-lookup"><span data-stu-id="ed593-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="ed593-104">Bestimmt die Richtung der Zeichen in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="ed593-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="ed593-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ed593-105">**Value**</span></span>|<span data-ttu-id="ed593-106">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="ed593-106">**Direction**</span></span>|<span data-ttu-id="ed593-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ed593-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ed593-108">0</span><span class="sxs-lookup"><span data-stu-id="ed593-108">0</span></span>  <br/> | <span data-ttu-id="ed593-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="ed593-109">Horizontal</span></span>  <br/> |<span data-ttu-id="ed593-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="ed593-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="ed593-111">1</span><span class="sxs-lookup"><span data-stu-id="ed593-111">1</span></span>  <br/> | <span data-ttu-id="ed593-112">Vertikal</span><span class="sxs-lookup"><span data-stu-id="ed593-112">Vertical</span></span>  <br/> |<span data-ttu-id="ed593-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="ed593-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed593-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed593-114">Remarks</span></span>

<span data-ttu-id="ed593-115">In der japanischen Ausgabe von Visio Version  5.0 wurde der Wert dieser Zelle in der Zelle VerticalText im Abschnitt Miscellaneous gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed593-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="ed593-116">Um einen Verweis auf die TextDirection-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="ed593-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed593-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ed593-117">Cell name:</span></span>  <br/> | <span data-ttu-id="ed593-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="ed593-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="ed593-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TextDirection-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ed593-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed593-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ed593-120">Section index:</span></span>  <br/> |<span data-ttu-id="ed593-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ed593-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed593-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ed593-122">Row index:</span></span>  <br/> |<span data-ttu-id="ed593-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="ed593-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="ed593-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ed593-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ed593-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="ed593-125">**visTxtBlkDirection**</span></span> <br/> |
   

