---
title: Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342882"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="91ddb-103">Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="91ddb-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="91ddb-104">Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird.</span><span class="sxs-lookup"><span data-stu-id="91ddb-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="91ddb-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91ddb-105">Remarks</span></span>

<span data-ttu-id="91ddb-106">Jeder Schatten hat eine schattierte Pin-Position, die ein Punkt auf dem Schatten ist, der der PIN des Shapes entspricht.</span><span class="sxs-lookup"><span data-stu-id="91ddb-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="91ddb-107">Wenn sich beispielsweise die PIN eines Shapes in der Mitte des Shapes befindet, ist die schattierte Position des Pins der Punkt in der Mitte des Schattens.</span><span class="sxs-lookup"><span data-stu-id="91ddb-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="91ddb-108">Wenn Sie die Skalierung auf einfache Schatten anwenden, wird die Vergrößerung an der schattierten Pin-Position zentriert. Wenn Sie die Skalierung auf schräge Schatten anwenden, wird die Vergrößerung in schräger Richtung angewendet.</span><span class="sxs-lookup"><span data-stu-id="91ddb-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="91ddb-109">Dieser Prozentsatz wird verwendet, wenn der Schattentyp für ein Shape auf Seiten Standard festgelegt ist (Zelle Cell Equals \* \* visFSTPageDefault \* \*).</span><span class="sxs-lookup"><span data-stu-id="91ddb-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals \*\* visFSTPageDefault \*\* ).</span></span> 
  
<span data-ttu-id="91ddb-110">Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="91ddb-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="91ddb-111">Dieser Wert entspricht dem Wert, den Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** im Feld **Vergrößerung** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**).</span><span class="sxs-lookup"><span data-stu-id="91ddb-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="91ddb-112">Wenn Sie einen Verweis auf die Zelle "ShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="91ddb-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91ddb-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="91ddb-113">Cell name:</span></span>  <br/> | <span data-ttu-id="91ddb-114">"ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="91ddb-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="91ddb-115">Wenn Sie einen Verweis auf die Zelle "ShdwScaleFactor aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="91ddb-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91ddb-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="91ddb-116">Section index:</span></span>  <br/> |<span data-ttu-id="91ddb-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91ddb-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="91ddb-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="91ddb-118">Row index:</span></span>  <br/> |<span data-ttu-id="91ddb-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="91ddb-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="91ddb-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="91ddb-120">Cell index:</span></span>  <br/> |<span data-ttu-id="91ddb-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="91ddb-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

