---
title: Zelle "ShdwOffsetX" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431652"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="b4560-103">Zelle "ShdwOffsetX" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="b4560-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="b4560-104">Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="b4560-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4560-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4560-105">Remarks</span></span>

<span data-ttu-id="b4560-p101">Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Bei Größenänderung der Zeichnung bleibt der Schattenabstand gleich.</span><span class="sxs-lookup"><span data-stu-id="b4560-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="b4560-109">Wenn Sie einen Verweis auf die Zelle "ShdwOffsetX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b4560-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4560-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b4560-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b4560-111">"ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="b4560-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="b4560-112">Wenn Sie einen Verweis auf die Zelle "ShdwOffsetX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b4560-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4560-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b4560-113">Section index:</span></span>  <br/> |<span data-ttu-id="b4560-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b4560-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b4560-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b4560-115">Row index:</span></span>  <br/> |<span data-ttu-id="b4560-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="b4560-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="b4560-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b4560-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b4560-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="b4560-118">**visPageShdwOffsetX**</span></span> <br/> |
   

