---
title: Zelle "noProofing" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Akzeptiert einen booleschen Wert.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357225"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="92558-104">Zelle "noProofing" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="92558-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="92558-105">Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="92558-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="92558-106">Akzeptiert einen **booleschen** Wert.</span><span class="sxs-lookup"><span data-stu-id="92558-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="92558-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="92558-107">**Value**</span></span>|<span data-ttu-id="92558-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92558-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92558-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="92558-109">TRUE</span></span>  <br/> |<span data-ttu-id="92558-110">Die Rechtschreibung wird nicht automatisch korrigiert, und es werden keine Rechtschreibfehler für das ausgewählte Shape angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92558-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="92558-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="92558-111">FALSE</span></span>  <br/> |<span data-ttu-id="92558-112">Die Rechtschreibung wird automatisch korrigiert, und Rechtschreibfehler werden für das ausgewählte Shape angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92558-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92558-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92558-113">Remarks</span></span>

<span data-ttu-id="92558-114">Wenn Sie einen Verweis auf die Zelle noProofing aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="92558-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92558-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="92558-115">Cell name:</span></span>  <br/> |<span data-ttu-id="92558-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="92558-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="92558-117">Wenn Sie einen Verweis auf die Zelle noProofing aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="92558-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92558-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="92558-118">Section index:</span></span>  <br/> |<span data-ttu-id="92558-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="92558-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="92558-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="92558-120">Row index:</span></span>  <br/> |<span data-ttu-id="92558-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="92558-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="92558-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="92558-122">Cell index:</span></span>  <br/> |<span data-ttu-id="92558-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="92558-123">**visObjNoProofing**</span></span> <br/> |
   

