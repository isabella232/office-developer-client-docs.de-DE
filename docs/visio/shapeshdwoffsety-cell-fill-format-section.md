---
title: Zelle "ShapeShdwOffsetY" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60077
localization_priority: Normal
ms.assetid: ef200f41-7b69-1291-f9df-a7035239a033
description: Legt den Abstand in Seiteneinheiten fest, den der Schatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: 669e15fd1badf9cf76decb117a9c4fb91e731271
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798042"
---
# <a name="shapeshdwoffsety-cell-fill-format-section"></a><span data-ttu-id="8281f-103">Zelle "ShapeShdwOffsetY" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="8281f-103">ShapeShdwOffsetY Cell (Fill Format Section)</span></span>

<span data-ttu-id="8281f-104">Legt den Abstand in Seiteneinheiten fest, den der Schatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="8281f-104">Determines the distance in page units that a shape's shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8281f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8281f-105">Remarks</span></span>

<span data-ttu-id="8281f-106">Dieser Wert entspricht dem Wert der Einstellung **Y-Abstand** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="8281f-106">This value corresponds to the value in the **Y Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="8281f-107">Wenn Sie einen Verweis auf die Zelle ShapeShdwOffsetY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8281f-107">To get a reference to the ShapeShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8281f-108">Zellenname</span><span class="sxs-lookup"><span data-stu-id="8281f-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8281f-109">ShapeShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="8281f-109">ShapeShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="8281f-110">Wenn Sie einen Verweis auf die Zelle ShapeShdwOffsetY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8281f-110">To get a reference to the ShapeShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8281f-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8281f-111">Section index:</span></span>  <br/> |<span data-ttu-id="8281f-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8281f-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8281f-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8281f-113">Row index:</span></span>  <br/> |<span data-ttu-id="8281f-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8281f-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="8281f-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8281f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8281f-116">**visFillShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="8281f-116">**visFillShdwOffsetY**</span></span> <br/> |
   

