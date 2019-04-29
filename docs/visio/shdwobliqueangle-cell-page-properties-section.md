---
title: Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430427"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="1f5df-103">Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="1f5df-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="1f5df-104">Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.</span><span class="sxs-lookup"><span data-stu-id="1f5df-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f5df-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f5df-105">Remarks</span></span>

<span data-ttu-id="1f5df-106">Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft und im Uhrzeigersinn gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="1f5df-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="1f5df-107">Der in dieser Zelle beschriebene Winkel wird verwendet, wenn die Zelle-Zelle (der Schattentyp für ein Shape auf dem Zeichenblatt) auf Seiten Standard (**visFSTPageDefault** ) festgelegt ist und der Schattentyp schräg ist.</span><span class="sxs-lookup"><span data-stu-id="1f5df-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="1f5df-108">Der standardmäßige Seiten Schattentyp wird in der Zelle "ShdwType definiert.</span><span class="sxs-lookup"><span data-stu-id="1f5df-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="1f5df-109">Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwObliqueAngle.</span><span class="sxs-lookup"><span data-stu-id="1f5df-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="1f5df-110">Wenn Sie einen Verweis auf die Zelle "ShdwObliqueAngle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f5df-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f5df-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f5df-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1f5df-112">"ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="1f5df-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="1f5df-113">Wenn Sie einen Verweis auf die Zelle "ShdwObliqueAngle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f5df-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f5df-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f5df-114">Section index:</span></span>  <br/> |<span data-ttu-id="1f5df-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f5df-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f5df-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f5df-116">Row index:</span></span>  <br/> |<span data-ttu-id="1f5df-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="1f5df-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="1f5df-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f5df-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1f5df-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="1f5df-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   

