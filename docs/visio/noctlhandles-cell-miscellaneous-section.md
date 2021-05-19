---
title: Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
ms.openlocfilehash: cbe4d6a8b6fdd4b66acf064884d20999ff7e3b4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416125"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a><span data-ttu-id="a3fb7-103">Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="a3fb7-103">NoCtlHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="a3fb7-104">Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-104">Switches the display of control handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="a3fb7-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a3fb7-105">**Value**</span></span>|<span data-ttu-id="a3fb7-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3fb7-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a3fb7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a3fb7-107">TRUE</span></span>  <br/> | <span data-ttu-id="a3fb7-108">Steuerpunkte werden nicht angezeigt, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-108">Control handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="a3fb7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a3fb7-109">FALSE</span></span>  <br/> | <span data-ttu-id="a3fb7-110">Steuerpunkte werden angezeigt, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-110">Control handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3fb7-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3fb7-111">Remarks</span></span>

<span data-ttu-id="a3fb7-112">Um einen Verweis auf die Zelle NoCtlHandles anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-112">To get a reference to the NoCtlHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3fb7-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a3fb7-114">NoCtlHandles</span><span class="sxs-lookup"><span data-stu-id="a3fb7-114">NoCtlHandles</span></span>  <br/> |
   
<span data-ttu-id="a3fb7-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NoCtlHandles-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-115">To get a reference to the NoCtlHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3fb7-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-116">Section index:</span></span>  <br/> |<span data-ttu-id="a3fb7-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a3fb7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a3fb7-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-118">Row index:</span></span>  <br/> |<span data-ttu-id="a3fb7-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="a3fb7-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="a3fb7-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a3fb7-121">**visNoCtlHandles**</span><span class="sxs-lookup"><span data-stu-id="a3fb7-121">**visNoCtlHandles**</span></span> <br/> |
   

