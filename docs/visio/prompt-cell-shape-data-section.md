---
title: Zelle "Prompt" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Gibt die Beschreibung oder Anweisung Text, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797732"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="66c95-103">Prompt Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="66c95-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="66c95-104">Gibt die Beschreibung oder Anweisung Text, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster **Shape-Daten** platziert wird.</span><span class="sxs-lookup"><span data-stu-id="66c95-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="66c95-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66c95-105">Remarks</span></span>

<span data-ttu-id="66c95-106">Wenn Sie einen Verweis auf die Zelle Prompt nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="66c95-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66c95-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="66c95-107">Cell name:</span></span>  <br/> | <span data-ttu-id="66c95-108">Eigenschaft.  *Name* . Auffordern Sie, wobei *Name* der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="66c95-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="66c95-109">Wenn Sie einen Verweis auf die Zelle Prompt aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="66c95-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66c95-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="66c95-110">Section index:</span></span>  <br/> |<span data-ttu-id="66c95-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="66c95-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="66c95-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="66c95-112">Row index:</span></span>  <br/> |<span data-ttu-id="66c95-113">**VisRowProp +** *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="66c95-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="66c95-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="66c95-114">Cell index:</span></span>  <br/> |<span data-ttu-id="66c95-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="66c95-115">**visCustPropsPrompt**</span></span> <br/> |
   

