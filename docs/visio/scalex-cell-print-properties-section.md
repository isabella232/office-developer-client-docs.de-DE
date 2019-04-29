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
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="b0343-103">Zelle "ScaleX" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="b0343-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="b0343-104">Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.</span><span class="sxs-lookup"><span data-stu-id="b0343-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0343-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0343-105">Remarks</span></span>

<span data-ttu-id="b0343-106">Dieser Wert wird nur verwendet, wenn der Wert der onPage-Zelle FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="b0343-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="b0343-107">Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem Wert entspricht, der im Dialogfeld **Seite einrichten** auf der Registerkarte **Druckeinrichtung** auf die Einstellung **Anpassen an** festgelegt ist (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="b0343-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="b0343-108">Wenn Sie einen Verweis auf die Zelle ScaleX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b0343-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0343-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b0343-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b0343-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="b0343-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="b0343-111">Wenn Sie einen Verweis auf die Zelle ScaleX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b0343-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0343-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b0343-112">Section index:</span></span>  <br/> |<span data-ttu-id="b0343-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b0343-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b0343-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b0343-114">Row index:</span></span>  <br/> |<span data-ttu-id="b0343-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b0343-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b0343-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b0343-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b0343-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="b0343-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

