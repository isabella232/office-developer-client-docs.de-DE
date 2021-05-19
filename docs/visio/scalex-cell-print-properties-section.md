---
title: Zelle "ScaleX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410210"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="aa9b0-103">Zelle "ScaleX" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="aa9b0-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="aa9b0-104">Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.</span><span class="sxs-lookup"><span data-stu-id="aa9b0-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa9b0-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa9b0-105">Remarks</span></span>

<span data-ttu-id="aa9b0-106">Dieser Wert wird nur verwendet, wenn der OnPage-Zellwert FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="aa9b0-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="aa9b0-107">Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem  Wert in  der Einstellung Anpassen an  auf der Registerkarte Setup drucken im Dialogfeld Seiteneinrichtung entspricht (klicken Sie auf der Registerkarte Entwurf auf den Pfeil Seite **einrichten).** </span><span class="sxs-lookup"><span data-stu-id="aa9b0-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="aa9b0-108">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ScaleX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="aa9b0-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa9b0-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="aa9b0-109">Cell name:</span></span>  <br/> |<span data-ttu-id="aa9b0-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="aa9b0-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="aa9b0-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ScaleX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="aa9b0-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa9b0-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="aa9b0-112">Section index:</span></span>  <br/> |<span data-ttu-id="aa9b0-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aa9b0-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="aa9b0-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="aa9b0-114">Row index:</span></span>  <br/> |<span data-ttu-id="aa9b0-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="aa9b0-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="aa9b0-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="aa9b0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="aa9b0-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="aa9b0-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

