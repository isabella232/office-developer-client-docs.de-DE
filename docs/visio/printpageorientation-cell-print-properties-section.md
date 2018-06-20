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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797738"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="1f8ea-103">Zelle "PrintPageOrientation" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="1f8ea-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="1f8ea-104">Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="1f8ea-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="1f8ea-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-105">**Value**</span></span>|<span data-ttu-id="1f8ea-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-106">**Orientation**</span></span>|<span data-ttu-id="1f8ea-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1f8ea-108">0</span><span class="sxs-lookup"><span data-stu-id="1f8ea-108">0</span></span>  <br/> | <span data-ttu-id="1f8ea-109">Druckereinstellungen übernehmen</span><span class="sxs-lookup"><span data-stu-id="1f8ea-109">Same as printer</span></span>  <br/> |<span data-ttu-id="1f8ea-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="1f8ea-111">1</span><span class="sxs-lookup"><span data-stu-id="1f8ea-111">1</span></span>  <br/> | <span data-ttu-id="1f8ea-112">Hochformat</span><span class="sxs-lookup"><span data-stu-id="1f8ea-112">Portrait</span></span>  <br/> |<span data-ttu-id="1f8ea-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="1f8ea-114">2</span><span class="sxs-lookup"><span data-stu-id="1f8ea-114">2</span></span>  <br/> |<span data-ttu-id="1f8ea-115">Querformat</span><span class="sxs-lookup"><span data-stu-id="1f8ea-115">Landscape</span></span>  <br/> |<span data-ttu-id="1f8ea-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f8ea-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f8ea-117">Remarks</span></span>

<span data-ttu-id="1f8ea-118">Beim Einfügen neuer Seiten in einem Dokument ist die Standardeinstellung die Einstellung in der aktiven Seite.</span><span class="sxs-lookup"><span data-stu-id="1f8ea-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="1f8ea-119">Wenn Sie einen Verweis auf die Zelle PrintPageOrientation nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f8ea-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f8ea-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f8ea-120">Cell name:</span></span>  <br/> | <span data-ttu-id="1f8ea-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="1f8ea-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="1f8ea-122">Wenn Sie einen Verweis auf die Zelle PrintPageOrientation aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f8ea-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f8ea-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f8ea-123">Section index:</span></span>  <br/> |<span data-ttu-id="1f8ea-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f8ea-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f8ea-125">Row index:</span></span>  <br/> |<span data-ttu-id="1f8ea-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="1f8ea-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f8ea-127">Cell index:</span></span>  <br/> |<span data-ttu-id="1f8ea-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="1f8ea-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

