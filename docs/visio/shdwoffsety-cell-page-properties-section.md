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
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349056"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="16495-103">Zelle "ShdwOffsetY" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="16495-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="16495-104">Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="16495-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16495-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16495-105">Remarks</span></span>

<span data-ttu-id="16495-p101">Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Bei Größenänderung der Zeichnung bleibt der Schattenabstand gleich.</span><span class="sxs-lookup"><span data-stu-id="16495-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="16495-109">Wenn Sie einen Verweis auf die Zelle "ShdwOffsetY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16495-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16495-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="16495-110">Cell name:</span></span>  <br/> | <span data-ttu-id="16495-111">"ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="16495-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="16495-112">Wenn Sie einen Verweis auf die Zelle "ShdwOffsetY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="16495-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16495-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="16495-113">Section index:</span></span>  <br/> |<span data-ttu-id="16495-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16495-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16495-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="16495-115">Row index:</span></span>  <br/> |<span data-ttu-id="16495-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="16495-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="16495-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="16495-117">Cell index:</span></span>  <br/> |<span data-ttu-id="16495-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="16495-118">**visPageShdwOffsetY**</span></span> <br/> |
   

