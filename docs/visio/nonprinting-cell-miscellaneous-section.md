---
title: Zelle "NonPrinting" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797545"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="755f9-103">NonPrinting Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="755f9-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="755f9-104">Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.</span><span class="sxs-lookup"><span data-stu-id="755f9-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="755f9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="755f9-105">**Value**</span></span>|<span data-ttu-id="755f9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="755f9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="755f9-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="755f9-107">TRUE</span></span>  <br/> | <span data-ttu-id="755f9-108">Das Drucken ist deaktiviert, doch das Shape wird im Zeichnungsfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="755f9-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="755f9-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="755f9-109">FALSE</span></span>  <br/> | <span data-ttu-id="755f9-110">Drucken ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="755f9-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="755f9-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="755f9-111">Remarks</span></span>

<span data-ttu-id="755f9-112">Sie können eine Führungslinie drucken, indem Sie sie auswählen und anschließend den Wert ihrer Zelle NonPrinting auf FALSE setzen.</span><span class="sxs-lookup"><span data-stu-id="755f9-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="755f9-113">Wenn Sie einen Verweis auf die Zelle NonPrinting nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="755f9-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="755f9-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="755f9-114">Cell name:</span></span>  <br/> | <span data-ttu-id="755f9-115">Nicht druckbare</span><span class="sxs-lookup"><span data-stu-id="755f9-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="755f9-116">Wenn Sie einen Verweis auf die Zelle NonPrinting aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="755f9-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="755f9-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="755f9-117">Section index:</span></span>  <br/> |<span data-ttu-id="755f9-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="755f9-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="755f9-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="755f9-119">Row index:</span></span>  <br/> |<span data-ttu-id="755f9-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="755f9-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="755f9-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="755f9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="755f9-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="755f9-122">**visNonPrinting**</span></span> <br/> |
   

