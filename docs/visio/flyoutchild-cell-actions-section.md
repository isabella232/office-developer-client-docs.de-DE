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
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420864"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="062e0-103">Zelle "FlyoutChild" (Abschnitt "Aktionen")</span><span class="sxs-lookup"><span data-stu-id="062e0-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="062e0-104">Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.</span><span class="sxs-lookup"><span data-stu-id="062e0-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="062e0-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="062e0-105">Remarks</span></span>

<span data-ttu-id="062e0-106">Verwenden Sie folgendes, um einen Verweis auf die FlyoutChild-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="062e0-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="062e0-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="062e0-107">Cell name:</span></span>  <br/> |<span data-ttu-id="062e0-108">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="062e0-108">Actions.</span></span> <span data-ttu-id="062e0-109">*Name*  . FlyoutChildwhere-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="062e0-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="062e0-110">*Name*  ist der Name der Zeile Aktionen</span><span class="sxs-lookup"><span data-stu-id="062e0-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="062e0-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die FlyoutChild-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="062e0-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="062e0-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="062e0-112">Section index:</span></span>  <br/> |<span data-ttu-id="062e0-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="062e0-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="062e0-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="062e0-114">Row index:</span></span>  <br/> |<span data-ttu-id="062e0-115">**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="062e0-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="062e0-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="062e0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="062e0-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="062e0-117">**visActionFlyoutChild**</span></span> <br/> |
   

