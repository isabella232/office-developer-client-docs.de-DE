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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332375"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="ae1ac-103">Zelle "TextDirection" (Abschnitt "Text Block Format ")</span><span class="sxs-lookup"><span data-stu-id="ae1ac-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="ae1ac-104">Bestimmt die Richtung der Zeichen in einem Textblock.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="ae1ac-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-105">**Value**</span></span>|<span data-ttu-id="ae1ac-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-106">**Direction**</span></span>|<span data-ttu-id="ae1ac-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ae1ac-108">0</span><span class="sxs-lookup"><span data-stu-id="ae1ac-108">0</span></span>  <br/> | <span data-ttu-id="ae1ac-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="ae1ac-109">Horizontal</span></span>  <br/> |<span data-ttu-id="ae1ac-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="ae1ac-111">1</span><span class="sxs-lookup"><span data-stu-id="ae1ac-111">1</span></span>  <br/> | <span data-ttu-id="ae1ac-112">Vertikal</span><span class="sxs-lookup"><span data-stu-id="ae1ac-112">Vertical</span></span>  <br/> |<span data-ttu-id="ae1ac-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae1ac-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae1ac-114">Remarks</span></span>

<span data-ttu-id="ae1ac-115">In der japanischen Ausgabe von Visio Version  5.0 wurde der Wert dieser Zelle in der Zelle VerticalText im Abschnitt Miscellaneous gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="ae1ac-116">Wenn Sie einen Verweis auf die Zelle textDirection aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae1ac-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-117">Cell name:</span></span>  <br/> | <span data-ttu-id="ae1ac-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="ae1ac-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="ae1ac-119">Wenn Sie einen Verweis auf die Zelle textDirection aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae1ac-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-120">Section index:</span></span>  <br/> |<span data-ttu-id="ae1ac-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ae1ac-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-122">Row index:</span></span>  <br/> |<span data-ttu-id="ae1ac-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="ae1ac-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ae1ac-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-125">**visTxtBlkDirection**</span></span> <br/> |
   

