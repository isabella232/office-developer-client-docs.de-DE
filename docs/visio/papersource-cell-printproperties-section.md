---
title: Zelle "PaperSource" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Bestimmt die Papierzufuhr für die Seite.
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406759"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="99340-103">Zelle "PaperSource" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="99340-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="99340-104">Bestimmt die Papierzufuhr für die Seite.</span><span class="sxs-lookup"><span data-stu-id="99340-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="99340-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99340-105">Remarks</span></span>

<span data-ttu-id="99340-106">Diese Einstellung entspricht der Einstellung **Papierzufuhr** im Dialogfeld **Druckeinrichtung** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** und anschließend auf der Registerkarte **Druckeinrichtung** auf **Einrichten**).</span><span class="sxs-lookup"><span data-stu-id="99340-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="99340-107">Die numerischen Werte in dieser Zelle ordnen Konstanten (mit DMBIN vorangestellt) zu, die für die Binauswahl in der Datei "Microsoft Windows wingdi.h" definiert sind. Beispielsweise steht der Wert 7 für DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="99340-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="99340-108">Um einen Verweis auf die Zelle PaperSource anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="99340-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99340-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="99340-109">Cell name:</span></span>  <br/> |<span data-ttu-id="99340-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="99340-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="99340-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PaperSource nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="99340-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99340-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="99340-112">Section index:</span></span>  <br/> |<span data-ttu-id="99340-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="99340-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="99340-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="99340-114">Row index:</span></span>  <br/> |<span data-ttu-id="99340-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="99340-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="99340-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="99340-116">Cell index:</span></span>  <br/> |<span data-ttu-id="99340-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="99340-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

