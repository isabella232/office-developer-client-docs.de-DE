---
title: Zelle "LineCap" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Gibt an, ob eine Linie abgerundete, viereckige oder erweiterte Enden hat.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425198"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="41ab5-103">Zelle "LineCap" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="41ab5-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="41ab5-104">Gibt an, ob eine Linie abgerundete, viereckige oder erweiterte Enden hat.</span><span class="sxs-lookup"><span data-stu-id="41ab5-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="41ab5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="41ab5-105">**Value**</span></span>|<span data-ttu-id="41ab5-106">**Formatvorlage für das Linienende**</span><span class="sxs-lookup"><span data-stu-id="41ab5-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41ab5-107">0</span><span class="sxs-lookup"><span data-stu-id="41ab5-107">0</span></span>  <br/> |<span data-ttu-id="41ab5-108">Gerundet</span><span class="sxs-lookup"><span data-stu-id="41ab5-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="41ab5-109">1</span><span class="sxs-lookup"><span data-stu-id="41ab5-109">1</span></span>  <br/> |<span data-ttu-id="41ab5-110">Square</span><span class="sxs-lookup"><span data-stu-id="41ab5-110">Square</span></span>  <br/> |
|<span data-ttu-id="41ab5-111">2</span><span class="sxs-lookup"><span data-stu-id="41ab5-111">2</span></span>  <br/> |<span data-ttu-id="41ab5-112">Erweitert</span><span class="sxs-lookup"><span data-stu-id="41ab5-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41ab5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41ab5-113">Remarks</span></span>

<span data-ttu-id="41ab5-114">Sie können den Wert dieser Zelle auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).</span><span class="sxs-lookup"><span data-stu-id="41ab5-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="41ab5-115">Wenn Sie einen Verweis auf die Zelle "LineCap aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="41ab5-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41ab5-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="41ab5-116">Cell name:</span></span>  <br/> |<span data-ttu-id="41ab5-117">"LineCap</span><span class="sxs-lookup"><span data-stu-id="41ab5-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="41ab5-118">Wenn Sie einen Verweis auf die Zelle "LineCap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="41ab5-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41ab5-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="41ab5-119">Section index:</span></span>  <br/> |<span data-ttu-id="41ab5-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41ab5-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="41ab5-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="41ab5-121">Row index:</span></span>  <br/> |<span data-ttu-id="41ab5-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="41ab5-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="41ab5-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="41ab5-123">Cell index:</span></span>  <br/> |<span data-ttu-id="41ab5-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="41ab5-124">**visLineEndCap**</span></span> <br/> |
   

