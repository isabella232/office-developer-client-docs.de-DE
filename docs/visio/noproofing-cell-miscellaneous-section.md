---
title: Zelle "NoProofing" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Nimmt einen booleschen Wert an.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431253"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="e51e4-104">Zelle "NoProofing" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="e51e4-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="e51e4-105">Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e51e4-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="e51e4-106">Nimmt einen **booleschen Wert** an.</span><span class="sxs-lookup"><span data-stu-id="e51e4-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="e51e4-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e51e4-107">**Value**</span></span>|<span data-ttu-id="e51e4-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e51e4-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e51e4-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="e51e4-109">TRUE</span></span>  <br/> |<span data-ttu-id="e51e4-110">Die Rechtschreibung wird nicht automatisch korrigiert, und Rechtschreibfehler werden für die ausgewählte Form nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e51e4-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="e51e4-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="e51e4-111">FALSE</span></span>  <br/> |<span data-ttu-id="e51e4-112">Die Rechtschreibung wird automatisch korrigiert, und Rechtschreibfehler werden für das ausgewählte Shape angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e51e4-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e51e4-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e51e4-113">Remarks</span></span>

<span data-ttu-id="e51e4-114">Verwenden Sie zum Erhalten eines Verweises auf die Zelle NoProofing anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="e51e4-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e51e4-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e51e4-115">Cell name:</span></span>  <br/> |<span data-ttu-id="e51e4-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="e51e4-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="e51e4-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NoProofing nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e51e4-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e51e4-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e51e4-118">Section index:</span></span>  <br/> |<span data-ttu-id="e51e4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e51e4-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e51e4-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e51e4-120">Row index:</span></span>  <br/> |<span data-ttu-id="e51e4-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="e51e4-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="e51e4-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e51e4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="e51e4-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="e51e4-123">**visObjNoProofing**</span></span> <br/> |
   

