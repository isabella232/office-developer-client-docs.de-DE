---
title: Zelle "FlyoutChild" (Abschnitt "Aktionen")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797030"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="b802d-103">Zelle "FlyoutChild" (Abschnitt "Aktionen")</span><span class="sxs-lookup"><span data-stu-id="b802d-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="b802d-104">Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.</span><span class="sxs-lookup"><span data-stu-id="b802d-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b802d-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b802d-105">Remarks</span></span>

<span data-ttu-id="b802d-106">Zum Abrufen eines Verweises auf die Zelle FlyoutChild nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes.</span><span class="sxs-lookup"><span data-stu-id="b802d-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b802d-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b802d-107">Cell name:</span></span>  <br/> |<span data-ttu-id="b802d-108">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="b802d-108">Actions.</span></span> <span data-ttu-id="b802d-109">*Name* . FlyoutChildwhere Aktionen.</span><span class="sxs-lookup"><span data-stu-id="b802d-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="b802d-110">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="b802d-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="b802d-111">Wenn Sie einen Verweis auf die Zelle FlyoutChild aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b802d-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b802d-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b802d-112">Section index:</span></span>  <br/> |<span data-ttu-id="b802d-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="b802d-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="b802d-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b802d-114">Row index:</span></span>  <br/> |<span data-ttu-id="b802d-115">**VisRowAction** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b802d-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b802d-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b802d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b802d-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="b802d-117">**visActionFlyoutChild**</span></span> <br/> |
   

