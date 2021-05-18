---
title: Zelle "PaperKind" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Gibt den Papiertyp für den Druck der Seite an.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408446"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="2610c-103">Zelle "PaperKind" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="2610c-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="2610c-104">Gibt den Papiertyp für den Druck der Seite an.</span><span class="sxs-lookup"><span data-stu-id="2610c-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2610c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2610c-105">Remarks</span></span>

<span data-ttu-id="2610c-106">Diese Einstellung entspricht  der Einstellung Papierformat im Dialogfeld  Druckeinrichtung (klicken  Sie auf der Registerkarte  Entwurf auf den Pfeil Seite einrichten, und klicken Sie dann auf der Registerkarte Druckeinrichtung auf die Schaltfläche **Setup).** </span><span class="sxs-lookup"><span data-stu-id="2610c-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="2610c-107">Die numerischen Werte in dieser Zelle ordnen Konstanten (mit DMPAPER vorangestellt) zu, die für die Papierauswahl in der Datei "Microsoft Windows wingdi.h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2610c-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="2610c-108">Um einen Verweis auf die Zelle PaperKind anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2610c-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2610c-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2610c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="2610c-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="2610c-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="2610c-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PaperKind nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2610c-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2610c-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2610c-112">Section index:</span></span>  <br/> |<span data-ttu-id="2610c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2610c-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2610c-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2610c-114">Row index:</span></span>  <br/> |<span data-ttu-id="2610c-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="2610c-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="2610c-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2610c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2610c-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="2610c-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

