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
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797593"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="dfeb0-103">PaperSource Cell (PrintProperties Section)</span><span class="sxs-lookup"><span data-stu-id="dfeb0-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="dfeb0-104">Bestimmt die Papierzufuhr für die Seite.</span><span class="sxs-lookup"><span data-stu-id="dfeb0-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dfeb0-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfeb0-105">Remarks</span></span>

<span data-ttu-id="dfeb0-106">Diese Einstellung entspricht der Einstellung **Papierzufuhr** im Dialogfeld **Drucker einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf der Registerkarte **Drucken Setup** auf **Setup**).</span><span class="sxs-lookup"><span data-stu-id="dfeb0-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="dfeb0-107">Die numerischen Werte in dieser Zelle auf Konstanten (mit dem Präfix DMBIN) in der Microsoft Windows-Datei wingdi.h definiert; Beispielsweise steht für den Wert 7 Papierauswahl.</span><span class="sxs-lookup"><span data-stu-id="dfeb0-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="dfeb0-108">Wenn Sie einen Verweis auf die Zelle PaperSource nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dfeb0-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfeb0-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dfeb0-109">Cell name:</span></span>  <br/> |<span data-ttu-id="dfeb0-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="dfeb0-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="dfeb0-111">Wenn Sie einen Verweis auf die Zelle PaperSource aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dfeb0-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfeb0-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dfeb0-112">Section index:</span></span>  <br/> |<span data-ttu-id="dfeb0-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfeb0-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dfeb0-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dfeb0-114">Row index:</span></span>  <br/> |<span data-ttu-id="dfeb0-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="dfeb0-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="dfeb0-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dfeb0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="dfeb0-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="dfeb0-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

