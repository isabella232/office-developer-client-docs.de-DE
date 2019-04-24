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
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342728"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="b3f9b-103">Zelle "ScaleY" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="b3f9b-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="b3f9b-104">Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3f9b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3f9b-105">Remarks</span></span>

<span data-ttu-id="b3f9b-106">Dieser Wert wird nur verwendet, wenn der Wert der onPage-Zelle FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="b3f9b-107">Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem Wert entspricht, der im Dialogfeld **Seite einrichten** auf der Registerkarte **Druckeinrichtung** auf die Einstellung **Anpassen an** festgelegt ist (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="b3f9b-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="b3f9b-108">Wenn Sie einen Verweis auf die Zelle ScaleY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f9b-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b3f9b-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="b3f9b-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="b3f9b-111">Wenn Sie einen Verweis auf die Zelle ScaleY nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f9b-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-112">Section index:</span></span>  <br/> |<span data-ttu-id="b3f9b-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3f9b-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b3f9b-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-114">Row index:</span></span>  <br/> |<span data-ttu-id="b3f9b-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b3f9b-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b3f9b-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b3f9b-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="b3f9b-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

