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
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798079"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="cf2fe-103">ShdwOffsetX Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="cf2fe-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="cf2fe-104">Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="cf2fe-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf2fe-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf2fe-105">Remarks</span></span>

<span data-ttu-id="cf2fe-106">Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="cf2fe-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="cf2fe-107">Dieser Wert ist unabhängig von der Skalierung der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="cf2fe-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="cf2fe-108">Wenn die Zeichnung skaliert wird, bleibt der Offset des Schattens gleich.</span><span class="sxs-lookup"><span data-stu-id="cf2fe-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="cf2fe-109">Wenn Sie einen Verweis auf die Zelle ShdwOffsetX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cf2fe-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf2fe-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cf2fe-110">Cell name:</span></span>  <br/> | <span data-ttu-id="cf2fe-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="cf2fe-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="cf2fe-112">Wenn Sie einen Verweis auf die Zelle ShdwOffsetX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="cf2fe-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf2fe-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cf2fe-113">Section index:</span></span>  <br/> |<span data-ttu-id="cf2fe-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf2fe-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cf2fe-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cf2fe-115">Row index:</span></span>  <br/> |<span data-ttu-id="cf2fe-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="cf2fe-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="cf2fe-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="cf2fe-117">Cell index:</span></span>  <br/> |<span data-ttu-id="cf2fe-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="cf2fe-118">**visPageShdwOffsetX**</span></span> <br/> |
   

