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
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798081"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="766a7-103">ShdwScaleFactor Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="766a7-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="766a7-104">Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird.</span><span class="sxs-lookup"><span data-stu-id="766a7-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="766a7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="766a7-105">Remarks</span></span>

<span data-ttu-id="766a7-106">Jeder Schatten weist eine schattierte Speicherorts eines Punkts auf der Schatten, die die Shape-PIN bis entspricht.</span><span class="sxs-lookup"><span data-stu-id="766a7-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="766a7-107">Wenn ein Shape-Pin in der Mitte des Shapes befindet, würde der schattierte Speicherort beispielsweise den Punkt in der Mitte des Schattens sein.</span><span class="sxs-lookup"><span data-stu-id="766a7-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="766a7-108">Skalierung auf einfache Schatten angewendet wird, wird an der Position schattierte Vergrößerung zentriert; Beim Skalieren einfache Schatten anwenden, wird die Vergrößerung in der Schräge angibt angewendet.</span><span class="sxs-lookup"><span data-stu-id="766a7-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="766a7-109">Dieser Prozentsatz wird verwendet, wenn der Schattentyp eines Shapes auf Seitenstandard festgelegt ist (Zelle ShapeShdwType ist gleich ** VisFSTPageDefault **).</span><span class="sxs-lookup"><span data-stu-id="766a7-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals ** visFSTPageDefault ** ).</span></span> 
  
<span data-ttu-id="766a7-110">Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="766a7-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="766a7-111">Dieser Wert entspricht dem Wert, den Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** im Feld **Vergrößerung** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**).</span><span class="sxs-lookup"><span data-stu-id="766a7-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="766a7-112">Wenn Sie einen Verweis auf die Zelle ShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="766a7-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="766a7-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="766a7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="766a7-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="766a7-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="766a7-115">Wenn Sie einen Verweis auf die Zelle ShdwScaleFactor aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="766a7-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="766a7-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="766a7-116">Section index:</span></span>  <br/> |<span data-ttu-id="766a7-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="766a7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="766a7-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="766a7-118">Row index:</span></span>  <br/> |<span data-ttu-id="766a7-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="766a7-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="766a7-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="766a7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="766a7-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="766a7-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

