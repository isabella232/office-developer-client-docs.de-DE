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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301463"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="9bbf2-103">Zelle "PaperSource" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="9bbf2-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="9bbf2-104">Bestimmt die Papierzufuhr für die Seite.</span><span class="sxs-lookup"><span data-stu-id="9bbf2-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9bbf2-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bbf2-105">Remarks</span></span>

<span data-ttu-id="9bbf2-106">Diese Einstellung entspricht der Einstellung **Papierzufuhr** im Dialogfeld **Druckeinrichtung** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** und anschließend auf der Registerkarte **Druckeinrichtung** auf **Einrichten**).</span><span class="sxs-lookup"><span data-stu-id="9bbf2-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="9bbf2-107">Die numerischen Werte in dieser Zelle werden Konstanten (vorangestellt mit DMBIN) zugeordnet, die für die bin-Auswahl in der Datei Microsoft Windows WinGDI. h definiert sind. der Wert 7 stellt beispielsweise DMBIN_AUTO dar.</span><span class="sxs-lookup"><span data-stu-id="9bbf2-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="9bbf2-108">Wenn Sie einen Verweis auf die Zelle PaperSource aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9bbf2-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bbf2-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9bbf2-109">Cell name:</span></span>  <br/> |<span data-ttu-id="9bbf2-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="9bbf2-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="9bbf2-111">Wenn Sie einen Verweis auf die Zelle PaperSource aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9bbf2-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bbf2-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9bbf2-112">Section index:</span></span>  <br/> |<span data-ttu-id="9bbf2-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9bbf2-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9bbf2-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9bbf2-114">Row index:</span></span>  <br/> |<span data-ttu-id="9bbf2-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="9bbf2-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="9bbf2-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9bbf2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9bbf2-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="9bbf2-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

