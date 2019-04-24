---
title: Zelle "NoAlignBox" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: Aktiviert bzw. deaktiviert die Anzeige des Auswahlrechtecks für das ausgewählte Shape.
ms.openlocfilehash: 2ff9f051df54f4d424589332b9fbaea973552edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319859"
---
# <a name="noalignbox-cell-miscellaneous-section"></a><span data-ttu-id="d27ef-103">Zelle "NoAlignBox" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="d27ef-103">NoAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="d27ef-104">Aktiviert bzw. deaktiviert die Anzeige des Auswahlrechtecks für das ausgewählte Shape.</span><span class="sxs-lookup"><span data-stu-id="d27ef-104">Switches the display of the selection rectangle on and off for the selected shape.</span></span>
  
|<span data-ttu-id="d27ef-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d27ef-105">**Value**</span></span>|<span data-ttu-id="d27ef-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d27ef-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d27ef-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d27ef-107">TRUE</span></span>  <br/> | <span data-ttu-id="d27ef-108">Markierungsrechteck wird nicht angezeigt, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d27ef-108">Selection rectangle is not displayed when the shape is selected.</span></span>  <br/> |
| <span data-ttu-id="d27ef-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d27ef-109">FALSE</span></span>  <br/> | <span data-ttu-id="d27ef-110">Markierungsrechteck wird angezeigt, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d27ef-110">Selection rectangle is displayed when the shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d27ef-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d27ef-111">Remarks</span></span>

<span data-ttu-id="d27ef-112">Wenn Sie einen Verweis auf die Zelle noAlignbox aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d27ef-112">To get a reference to the NoAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d27ef-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d27ef-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d27ef-114">Zelle NoAlignBox</span><span class="sxs-lookup"><span data-stu-id="d27ef-114">NoAlignBox</span></span>  <br/> |
   
<span data-ttu-id="d27ef-115">Wenn Sie einen Verweis auf die Zelle noAlignbox nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d27ef-115">To get a reference to the NoAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d27ef-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d27ef-116">Section index:</span></span>  <br/> |<span data-ttu-id="d27ef-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d27ef-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d27ef-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d27ef-118">Row index:</span></span>  <br/> |<span data-ttu-id="d27ef-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="d27ef-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="d27ef-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d27ef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d27ef-121">**visNoAlignBox**</span><span class="sxs-lookup"><span data-stu-id="d27ef-121">**visNoAlignBox**</span></span> <br/> |
   

