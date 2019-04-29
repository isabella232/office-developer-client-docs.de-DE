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
description: Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405485"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="55d05-103">Zelle "Prompt" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="55d05-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="55d05-104">Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster **Shape-Daten** platziert wird.</span><span class="sxs-lookup"><span data-stu-id="55d05-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="55d05-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55d05-105">Remarks</span></span>

<span data-ttu-id="55d05-106">Wenn Sie einen Verweis auf die Zelle "Ansage" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55d05-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55d05-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="55d05-107">Cell name:</span></span>  <br/> | <span data-ttu-id="55d05-108">Prop.  *Name* . AufFordern, wobei *Name* der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="55d05-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="55d05-109">Wenn Sie einen Verweis auf die Zelle "anSagen" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="55d05-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55d05-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="55d05-110">Section index:</span></span>  <br/> |<span data-ttu-id="55d05-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="55d05-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="55d05-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="55d05-112">Row index:</span></span>  <br/> |<span data-ttu-id="55d05-113">**visRowProp +** *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="55d05-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="55d05-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="55d05-114">Cell index:</span></span>  <br/> |<span data-ttu-id="55d05-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="55d05-115">**visCustPropsPrompt**</span></span> <br/> |
   

