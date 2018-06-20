---
title: Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Bestimmt die Bedingungen für einen Verbindersprung.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796712"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="ca708-103">ConLineJumpCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="ca708-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ca708-104">Bestimmt die Bedingungen für einen Verbindersprung.</span><span class="sxs-lookup"><span data-stu-id="ca708-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="ca708-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ca708-105">**Value**</span></span>|<span data-ttu-id="ca708-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca708-106">**Description**</span></span>|<span data-ttu-id="ca708-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ca708-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca708-108">0</span><span class="sxs-lookup"><span data-stu-id="ca708-108">0</span></span>  <br/> |<span data-ttu-id="ca708-109">Nach Blattvorgabe; Klicken Sie auf den Pfeil in der Gruppe **Seite einrichten** auf der Registerkarte **Entwurf** , und klicken Sie dann auf die Registerkarte **Layout und Routing** , um die Seite Spezifikationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="ca708-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="ca708-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="ca708-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="ca708-111">1</span><span class="sxs-lookup"><span data-stu-id="ca708-111">1</span></span>  <br/> |<span data-ttu-id="ca708-112">Nie</span><span class="sxs-lookup"><span data-stu-id="ca708-112">Never</span></span>  <br/> |<span data-ttu-id="ca708-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="ca708-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="ca708-114">2</span><span class="sxs-lookup"><span data-stu-id="ca708-114">2</span></span>  <br/> |<span data-ttu-id="ca708-115">Immer</span><span class="sxs-lookup"><span data-stu-id="ca708-115">Always</span></span>  <br/> |<span data-ttu-id="ca708-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="ca708-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="ca708-117">3</span><span class="sxs-lookup"><span data-stu-id="ca708-117">3</span></span>  <br/> |<span data-ttu-id="ca708-118">Andere Verbindersprünge</span><span class="sxs-lookup"><span data-stu-id="ca708-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="ca708-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="ca708-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="ca708-120">4</span><span class="sxs-lookup"><span data-stu-id="ca708-120">4</span></span>  <br/> |<span data-ttu-id="ca708-121">Keine Verbindersprünge</span><span class="sxs-lookup"><span data-stu-id="ca708-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="ca708-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="ca708-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca708-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca708-123">Remarks</span></span>

<span data-ttu-id="ca708-124">Sie können auch den Wert für diese Zelle festlegen einen dynamischen Verbinder, indem Sie in der Gruppe **Shape-Design** auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** .</span><span class="sxs-lookup"><span data-stu-id="ca708-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="ca708-125">Zum Abrufen eines Verweises auf die Zelle ConLineJumpCode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ca708-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca708-126">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ca708-126">Cell name:</span></span>  <br/> |<span data-ttu-id="ca708-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="ca708-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="ca708-128">Wenn Sie einen Verweis auf die Zelle ConLineJumpCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ca708-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca708-129">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ca708-129">Section index:</span></span>  <br/> |<span data-ttu-id="ca708-130">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca708-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ca708-131">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ca708-131">Row index:</span></span>  <br/> |<span data-ttu-id="ca708-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ca708-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="ca708-133">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ca708-133">Cell index:</span></span>  <br/> |<span data-ttu-id="ca708-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="ca708-134">**visSLOJumpCode**</span></span> <br/> |
   

