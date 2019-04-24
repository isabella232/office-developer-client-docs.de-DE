---
title: Zelle "Tip" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307721"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="a896a-104">Zelle "Tip" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="a896a-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="a896a-p102">Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a896a-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a896a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a896a-107">Remarks</span></span>

<span data-ttu-id="a896a-108">Wenn Sie einen Verweis auf die Zelle Tip aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a896a-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a896a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a896a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a896a-110">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a896a-110">Controls.</span></span>  <span data-ttu-id="a896a-111">*Name* . Tipwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a896a-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="a896a-112">*Name* ist der Name der Zeile Controls.</span><span class="sxs-lookup"><span data-stu-id="a896a-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="a896a-113">Wenn Sie einen Verweis auf die Zelle Tip aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a896a-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a896a-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a896a-114">Section index:</span></span>  <br/> |<span data-ttu-id="a896a-115">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="a896a-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="a896a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a896a-116">Row index:</span></span>  <br/> |<span data-ttu-id="a896a-117">**visRowControl** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a896a-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a896a-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a896a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a896a-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="a896a-119">**visCtlTip**</span></span> <br/> |
   

