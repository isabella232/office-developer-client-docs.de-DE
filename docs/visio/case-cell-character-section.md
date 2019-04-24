---
title: Zelle "Case" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Bestimmt die Groß- und Kleinschreibung für den Text des Shapes. Die Optionen Nur Großbuchstaben (1) und Große Anfangsbuchstaben (2) ändern die Darstellung eines komplett in Großbuchstaben eingegebenen Texts nicht. Der Text muss in Kleinbuchstaben eingegeben werden, damit diese Optionen eine Wirkung zeigen.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337233"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="8ed94-105">Zelle "Case" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="8ed94-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="8ed94-p102">Bestimmt die Groß- und Kleinschreibung für den Text des Shapes. Die Optionen Nur Großbuchstaben (1) und Große Anfangsbuchstaben (2) ändern die Darstellung eines komplett in Großbuchstaben eingegebenen Texts nicht. Der Text muss in Kleinbuchstaben eingegeben werden, damit diese Optionen eine Wirkung zeigen.</span><span class="sxs-lookup"><span data-stu-id="8ed94-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="8ed94-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8ed94-109">**Value**</span></span>|<span data-ttu-id="8ed94-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ed94-110">**Description**</span></span>|<span data-ttu-id="8ed94-111">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="8ed94-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8ed94-112">0</span><span class="sxs-lookup"><span data-stu-id="8ed94-112">0</span></span>  <br/> | <span data-ttu-id="8ed94-113">Normalschreibung</span><span class="sxs-lookup"><span data-stu-id="8ed94-113">Normal case</span></span>  <br/> |<span data-ttu-id="8ed94-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="8ed94-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="8ed94-115">1</span><span class="sxs-lookup"><span data-stu-id="8ed94-115">1</span></span>  <br/> | <span data-ttu-id="8ed94-116">Nur Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="8ed94-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="8ed94-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="8ed94-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="8ed94-118">2</span><span class="sxs-lookup"><span data-stu-id="8ed94-118">2</span></span>  <br/> | <span data-ttu-id="8ed94-119">Große Anfangsbuchstaben</span><span class="sxs-lookup"><span data-stu-id="8ed94-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="8ed94-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="8ed94-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed94-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ed94-121">Remarks</span></span>

<span data-ttu-id="8ed94-122">Wenn Sie einen Verweis auf die Zelle Case aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8ed94-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ed94-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8ed94-123">Cell name:</span></span>  <br/> | <span data-ttu-id="8ed94-124">Char. Case [ *i* ] wobei *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="8ed94-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="8ed94-125">Wenn Sie einen Verweis auf die Zelle Case aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8ed94-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ed94-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8ed94-126">Section index:</span></span>  <br/> |<span data-ttu-id="8ed94-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8ed94-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="8ed94-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8ed94-128">Row index:</span></span>  <br/> |<span data-ttu-id="8ed94-129">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="8ed94-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="8ed94-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8ed94-130">Cell index:</span></span>  <br/> |<span data-ttu-id="8ed94-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="8ed94-131">**visCharacterCase**</span></span> <br/> |
   

