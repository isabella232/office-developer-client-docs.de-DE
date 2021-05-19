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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424861"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="9c506-104">Zelle "Tip" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="9c506-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="9c506-p102">Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c506-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c506-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c506-107">Remarks</span></span>

<span data-ttu-id="9c506-108">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Tip anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="9c506-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c506-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9c506-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9c506-110">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="9c506-110">Controls.</span></span>  <span data-ttu-id="9c506-111">*Name*  . Tipwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="9c506-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="9c506-112">*name*  ist der Name der Steuerelementzeile.</span><span class="sxs-lookup"><span data-stu-id="9c506-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="9c506-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Tip nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9c506-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c506-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9c506-114">Section index:</span></span>  <br/> |<span data-ttu-id="9c506-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="9c506-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="9c506-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9c506-116">Row index:</span></span>  <br/> |<span data-ttu-id="9c506-117">**visRowControl**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9c506-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9c506-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9c506-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9c506-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="9c506-119">**visCtlTip**</span></span> <br/> |
   

