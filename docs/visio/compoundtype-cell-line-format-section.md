---
title: Zusammengesetzte Zelle (Abschnitt "Linien Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Bestimmt den zusammengesetzten Typ der Form.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407172"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="ba6e9-103">Zusammengesetzte Zelle (Abschnitt "Linien Format")</span><span class="sxs-lookup"><span data-stu-id="ba6e9-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="ba6e9-104">Bestimmt den zusammengesetzten Typ der Form.</span><span class="sxs-lookup"><span data-stu-id="ba6e9-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="ba6e9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ba6e9-105">**Value**</span></span>|<span data-ttu-id="ba6e9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba6e9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba6e9-107">0</span><span class="sxs-lookup"><span data-stu-id="ba6e9-107">0</span></span>  <br/> |<span data-ttu-id="ba6e9-108">Einfach</span><span class="sxs-lookup"><span data-stu-id="ba6e9-108">Simple</span></span>  <br/> |
|<span data-ttu-id="ba6e9-109">1</span><span class="sxs-lookup"><span data-stu-id="ba6e9-109">1</span></span>  <br/> |<span data-ttu-id="ba6e9-110">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="ba6e9-110">Double</span></span>  <br/> |
|<span data-ttu-id="ba6e9-111">2</span><span class="sxs-lookup"><span data-stu-id="ba6e9-111">2</span></span>  <br/> |<span data-ttu-id="ba6e9-112">Dünn</span><span class="sxs-lookup"><span data-stu-id="ba6e9-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="ba6e9-113">3</span><span class="sxs-lookup"><span data-stu-id="ba6e9-113">3</span></span>  <br/> |<span data-ttu-id="ba6e9-114">Dünn</span><span class="sxs-lookup"><span data-stu-id="ba6e9-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="ba6e9-115">4</span><span class="sxs-lookup"><span data-stu-id="ba6e9-115">4</span></span>  <br/> |<span data-ttu-id="ba6e9-116">Triple</span><span class="sxs-lookup"><span data-stu-id="ba6e9-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba6e9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba6e9-117">Remarks</span></span>

<span data-ttu-id="ba6e9-118">Wenn Sie einen Verweis auf die \*\*\*\* Zelle compoundtype aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ba6e9-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba6e9-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ba6e9-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ba6e9-120">Compoundtype</span><span class="sxs-lookup"><span data-stu-id="ba6e9-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="ba6e9-121">Wenn Sie einen Verweis auf die \*\*\*\* Zelle compoundtype nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ba6e9-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba6e9-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ba6e9-122">Section index:</span></span>  <br/> |<span data-ttu-id="ba6e9-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ba6e9-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ba6e9-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ba6e9-124">Row index:</span></span>  <br/> |<span data-ttu-id="ba6e9-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="ba6e9-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="ba6e9-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ba6e9-126">Cell index:</span></span>  <br/> |<span data-ttu-id="ba6e9-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="ba6e9-127">**visCompoundType**</span></span> <br/> |
   

