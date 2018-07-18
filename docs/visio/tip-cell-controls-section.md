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
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798287"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="3902f-104">Tip Cell (Controls Section)</span><span class="sxs-lookup"><span data-stu-id="3902f-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="3902f-p102">Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3902f-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3902f-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3902f-107">Remarks</span></span>

<span data-ttu-id="3902f-108">Wenn Sie einen Verweis auf die Zelle Tip aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3902f-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3902f-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3902f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="3902f-110">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3902f-110">Controls.</span></span>  <span data-ttu-id="3902f-111">*Name* . Tipwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3902f-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="3902f-112">*Name* ist der Name der Zeile mit Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="3902f-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="3902f-113">Wenn Sie einen Verweis auf die Zelle Tip aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3902f-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3902f-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3902f-114">Section index:</span></span>  <br/> |<span data-ttu-id="3902f-115">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="3902f-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="3902f-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3902f-116">Row index:</span></span>  <br/> |<span data-ttu-id="3902f-117">**VisRowControl** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3902f-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3902f-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3902f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="3902f-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="3902f-119">**visCtlTip**</span></span> <br/> |
   

