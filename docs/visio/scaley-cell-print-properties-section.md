---
title: Zelle "ScaleY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckseite an.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797970"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="03d9a-103">ScaleY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="03d9a-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="03d9a-104">Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckseite an.</span><span class="sxs-lookup"><span data-stu-id="03d9a-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03d9a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03d9a-105">Remarks</span></span>

<span data-ttu-id="03d9a-106">Dieser Wert wird nur, wenn der Wert der Zelle OnPage auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03d9a-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="03d9a-107">Die Zellen ScaleX und ScaleY haben immer den gleichen Wert dem Wert der Einstellung **Verkleinern** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten entspricht** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="03d9a-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="03d9a-108">Wenn Sie einen Verweis auf die Zelle ScaleY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="03d9a-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03d9a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="03d9a-109">Cell name:</span></span>  <br/> |<span data-ttu-id="03d9a-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="03d9a-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="03d9a-111">Wenn Sie einen Verweis auf die Zelle ScaleY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="03d9a-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03d9a-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="03d9a-112">Section index:</span></span>  <br/> |<span data-ttu-id="03d9a-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="03d9a-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="03d9a-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="03d9a-114">Row index:</span></span>  <br/> |<span data-ttu-id="03d9a-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="03d9a-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="03d9a-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="03d9a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="03d9a-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="03d9a-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

