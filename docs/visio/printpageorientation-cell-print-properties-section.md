---
title: Zelle "PrintPageOrientation" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434865"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="b131b-103">Zelle "PrintPageOrientation" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="b131b-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="b131b-104">Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="b131b-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="b131b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b131b-105">**Value**</span></span>|<span data-ttu-id="b131b-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="b131b-106">**Orientation**</span></span>|<span data-ttu-id="b131b-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b131b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b131b-108">0</span><span class="sxs-lookup"><span data-stu-id="b131b-108">0</span></span>  <br/> | <span data-ttu-id="b131b-109">Druckereinstellungen übernehmen</span><span class="sxs-lookup"><span data-stu-id="b131b-109">Same as printer</span></span>  <br/> |<span data-ttu-id="b131b-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="b131b-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="b131b-111">1</span><span class="sxs-lookup"><span data-stu-id="b131b-111">1</span></span>  <br/> | <span data-ttu-id="b131b-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="b131b-112">Portrait</span></span>  <br/> |<span data-ttu-id="b131b-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="b131b-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="b131b-114">2</span><span class="sxs-lookup"><span data-stu-id="b131b-114">2</span></span>  <br/> |<span data-ttu-id="b131b-115">Landschaft</span><span class="sxs-lookup"><span data-stu-id="b131b-115">Landscape</span></span>  <br/> |<span data-ttu-id="b131b-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="b131b-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b131b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b131b-117">Remarks</span></span>

<span data-ttu-id="b131b-118">Wenn Sie neue Seiten in ein Dokument einfügen, ist diese Einstellung standardmäßig die Einstellung auf der aktiven Seite.</span><span class="sxs-lookup"><span data-stu-id="b131b-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="b131b-119">Wenn Sie einen Verweis auf die Zelle PrintPageOrientation aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b131b-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b131b-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b131b-120">Cell name:</span></span>  <br/> | <span data-ttu-id="b131b-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="b131b-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="b131b-122">Wenn Sie einen Verweis auf die Zelle PrintPageOrientation aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b131b-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b131b-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b131b-123">Section index:</span></span>  <br/> |<span data-ttu-id="b131b-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b131b-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b131b-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b131b-125">Row index:</span></span>  <br/> |<span data-ttu-id="b131b-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b131b-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="b131b-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b131b-127">Cell index:</span></span>  <br/> |<span data-ttu-id="b131b-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="b131b-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

