---
title: Zelle "ShdwOffsetY" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798096"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="b6432-103">ShdwOffsetY Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b6432-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="b6432-104">Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="b6432-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6432-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6432-105">Remarks</span></span>

<span data-ttu-id="b6432-p101">Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Bei Größenänderung der Zeichnung bleibt der Schattenabstand gleich.</span><span class="sxs-lookup"><span data-stu-id="b6432-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="b6432-109">Wenn Sie einen Verweis auf die Zelle ShdwOffsetY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b6432-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6432-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b6432-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b6432-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="b6432-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="b6432-112">Wenn Sie einen Verweis auf die Zelle ShdwOffsetY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b6432-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6432-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b6432-113">Section index:</span></span>  <br/> |<span data-ttu-id="b6432-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6432-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b6432-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b6432-115">Row index:</span></span>  <br/> |<span data-ttu-id="b6432-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="b6432-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="b6432-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b6432-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b6432-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="b6432-118">**visPageShdwOffsetY**</span></span> <br/> |
   

