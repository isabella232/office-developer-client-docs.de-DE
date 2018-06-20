---
title: Zelle "ShapeShdwOffsetX" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60076
localization_priority: Normal
ms.assetid: a426f471-d35f-ef87-4c59-2c007ec2653f
description: Legt den Abstand in Seiteneinheiten fest, den der Schatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: 12512ce9edf49f91c786c3cd50baa8d07498a3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798052"
---
# <a name="shapeshdwoffsetx-cell-fill-format-section"></a><span data-ttu-id="38ee3-103">Zelle "ShapeShdwOffsetX" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="38ee3-103">ShapeShdwOffsetX Cell (Fill Format Section)</span></span>

<span data-ttu-id="38ee3-104">Legt den Abstand in Seiteneinheiten fest, den der Schatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="38ee3-104">Determines the distance in page units that a shape's shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38ee3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38ee3-105">Remarks</span></span>

<span data-ttu-id="38ee3-106">Dieser Wert entspricht dem Wert der Einstellung **X-Abstand** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="38ee3-106">This value corresponds to the value in the **X Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="38ee3-107">Wenn Sie einen Verweis auf die Zelle ShapeShdwOffsetX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="38ee3-107">To get a reference to the ShapeShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38ee3-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="38ee3-108">Cell name:</span></span>  <br/> | <span data-ttu-id="38ee3-109">ShapeShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="38ee3-109">ShapeShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="38ee3-110">Wenn Sie einen Verweis auf die Zelle ShapeShdwOffsetX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="38ee3-110">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38ee3-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="38ee3-111">Section index:</span></span>  <br/> |<span data-ttu-id="38ee3-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="38ee3-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="38ee3-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="38ee3-113">Row index:</span></span>  <br/> |<span data-ttu-id="38ee3-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="38ee3-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="38ee3-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="38ee3-115">Cell index:</span></span>  <br/> |<span data-ttu-id="38ee3-116">**visFillShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="38ee3-116">**visFillShdwOffsetX**</span></span> <br/> |
   

