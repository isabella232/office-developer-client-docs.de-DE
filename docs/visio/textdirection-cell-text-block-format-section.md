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
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798267"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="f80cf-103">TextDirection Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="f80cf-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="f80cf-104">Bestimmt die Richtung der Zeichen in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="f80cf-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="f80cf-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f80cf-105">**Value**</span></span>|<span data-ttu-id="f80cf-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="f80cf-106">**Direction**</span></span>|<span data-ttu-id="f80cf-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="f80cf-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f80cf-108">0</span><span class="sxs-lookup"><span data-stu-id="f80cf-108">0</span></span>  <br/> | <span data-ttu-id="f80cf-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="f80cf-109">Horizontal</span></span>  <br/> |<span data-ttu-id="f80cf-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="f80cf-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="f80cf-111">1</span><span class="sxs-lookup"><span data-stu-id="f80cf-111">1</span></span>  <br/> | <span data-ttu-id="f80cf-112">Vertikal</span><span class="sxs-lookup"><span data-stu-id="f80cf-112">Vertical</span></span>  <br/> |<span data-ttu-id="f80cf-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="f80cf-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f80cf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f80cf-114">Remarks</span></span>

<span data-ttu-id="f80cf-115">In der japanischen Ausgabe von Visio Version  5.0 wurde der Wert dieser Zelle in der Zelle VerticalText im Abschnitt Miscellaneous gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f80cf-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="f80cf-116">Wenn Sie einen Verweis auf die Zelle TextDirection nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f80cf-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f80cf-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f80cf-117">Cell name:</span></span>  <br/> | <span data-ttu-id="f80cf-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="f80cf-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="f80cf-119">Wenn Sie einen Verweis auf die Zelle TextDirection aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f80cf-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f80cf-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f80cf-120">Section index:</span></span>  <br/> |<span data-ttu-id="f80cf-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f80cf-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f80cf-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f80cf-122">Row index:</span></span>  <br/> |<span data-ttu-id="f80cf-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="f80cf-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="f80cf-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f80cf-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f80cf-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="f80cf-125">**visTxtBlkDirection**</span></span> <br/> |
   

