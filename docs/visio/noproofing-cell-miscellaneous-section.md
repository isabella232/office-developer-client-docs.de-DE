---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Nimmt einen booleschen Wert an.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19797547"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="58f61-104">NoProofing Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="58f61-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="58f61-105">Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58f61-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="58f61-106">Nimmt einen **booleschen** Wert an.</span><span class="sxs-lookup"><span data-stu-id="58f61-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="58f61-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="58f61-107">**Value**</span></span>|<span data-ttu-id="58f61-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58f61-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58f61-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="58f61-109">TRUE</span></span>  <br/> |<span data-ttu-id="58f61-110">Rechtschreibung wird nicht automatisch korrigiert und Rechtschreibfehler werden nicht für die markierte Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58f61-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="58f61-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="58f61-111">FALSE</span></span>  <br/> |<span data-ttu-id="58f61-112">Rechtschreibung wird automatisch korrigiert und Rechtschreibfehler für das ausgewählte Shape angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58f61-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58f61-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58f61-113">Remarks</span></span>

<span data-ttu-id="58f61-114">Zum Abrufen eines Verweises auf die Zelle NoProofing nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="58f61-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58f61-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="58f61-115">Cell name:</span></span>  <br/> |<span data-ttu-id="58f61-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="58f61-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="58f61-117">Wenn Sie einen Verweis auf die Zelle NoProofing aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="58f61-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58f61-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="58f61-118">Section index:</span></span>  <br/> |<span data-ttu-id="58f61-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58f61-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="58f61-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="58f61-120">Row index:</span></span>  <br/> |<span data-ttu-id="58f61-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="58f61-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="58f61-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="58f61-122">Cell index:</span></span>  <br/> |<span data-ttu-id="58f61-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="58f61-123">**visObjNoProofing**</span></span> <br/> |
   

