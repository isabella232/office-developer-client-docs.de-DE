---
title: Zelle "Relationships" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Speichert die Beziehungen zwischen Containern, Listen, Beschriftungen und Shapes.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359969"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="2c732-103">Zelle "Relationships" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="2c732-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="2c732-104">Speichert die Beziehungen zwischen Containern, Listen, Beschriftungen und Shapes.</span><span class="sxs-lookup"><span data-stu-id="2c732-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2c732-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c732-105">Remarks</span></span>

 <span data-ttu-id="2c732-106">Microsoft Visio verwendet die Zelle "Beziehungen" zum Speichern der Beziehungen, die dieses Shape betreffen.</span><span class="sxs-lookup"><span data-stu-id="2c732-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="2c732-107">Zum Darstellen der Beziehungen zu diesem Shape wird eine Reihe von DEPENDSON-Funktionen mit den angegebenen Parametern verwendet, wie in der nachstehenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2c732-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="2c732-108">**Erster Parameter**</span><span class="sxs-lookup"><span data-stu-id="2c732-108">**First parameter**</span></span>|<span data-ttu-id="2c732-109">**Zusätzliche Parameter**</span><span class="sxs-lookup"><span data-stu-id="2c732-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c732-110">1</span><span class="sxs-lookup"><span data-stu-id="2c732-110">1</span></span>  <br/> |<span data-ttu-id="2c732-111">Shapes, die Elemente dieses Containers sind</span><span class="sxs-lookup"><span data-stu-id="2c732-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="2c732-112">2</span><span class="sxs-lookup"><span data-stu-id="2c732-112">2</span></span>  <br/> |<span data-ttu-id="2c732-113">Shapes, die Elemente dieser Liste sind</span><span class="sxs-lookup"><span data-stu-id="2c732-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="2c732-114">3</span><span class="sxs-lookup"><span data-stu-id="2c732-114">3</span></span>  <br/> |<span data-ttu-id="2c732-115">Beschriftungen, die mit diesem Shape verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="2c732-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="2c732-116">4</span><span class="sxs-lookup"><span data-stu-id="2c732-116">4</span></span>  <br/> |<span data-ttu-id="2c732-117">Container, zu deren Elementen dieses Shape gehört</span><span class="sxs-lookup"><span data-stu-id="2c732-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="2c732-118">5</span><span class="sxs-lookup"><span data-stu-id="2c732-118">5</span></span>  <br/> |<span data-ttu-id="2c732-119">Listen, zu denen dieses Listenelement gehört</span><span class="sxs-lookup"><span data-stu-id="2c732-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="2c732-120">6</span><span class="sxs-lookup"><span data-stu-id="2c732-120">6</span></span>  <br/> |<span data-ttu-id="2c732-121">Shape, das mit dieser Beschriftung verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="2c732-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="2c732-122">7</span><span class="sxs-lookup"><span data-stu-id="2c732-122">7</span></span>  <br/> |<span data-ttu-id="2c732-123">Container an der linken Begrenzungskante, an der sich dieses Shape befindet</span><span class="sxs-lookup"><span data-stu-id="2c732-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="2c732-124">8</span><span class="sxs-lookup"><span data-stu-id="2c732-124">8</span></span>  <br/> |<span data-ttu-id="2c732-125">Container an der rechten Begrenzungskante, an der sich dieses Shape befindet</span><span class="sxs-lookup"><span data-stu-id="2c732-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="2c732-126">9</span><span class="sxs-lookup"><span data-stu-id="2c732-126">9</span></span>  <br/> |<span data-ttu-id="2c732-127">Container an der oberen Begrenzungskante, an der sich dieses Shape befindet</span><span class="sxs-lookup"><span data-stu-id="2c732-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="2c732-128">10</span><span class="sxs-lookup"><span data-stu-id="2c732-128">10</span></span>  <br/> |<span data-ttu-id="2c732-129">Container an der unteren Begrenzungskante, an der sich dieses Shape befindet</span><span class="sxs-lookup"><span data-stu-id="2c732-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="2c732-130">11</span><span class="sxs-lookup"><span data-stu-id="2c732-130">11</span></span>  <br/> |<span data-ttu-id="2c732-131">Liste, die von dieser Liste überlappt wird</span><span class="sxs-lookup"><span data-stu-id="2c732-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="2c732-132">Wenn Sie einen Verweis auf die Zelle Beziehungen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2c732-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c732-133">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2c732-133">Cell name:</span></span>  <br/> |<span data-ttu-id="2c732-134">Beziehungen</span><span class="sxs-lookup"><span data-stu-id="2c732-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="2c732-135">Wenn Sie einen Verweis auf die Zelle Beziehungen nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2c732-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c732-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2c732-136">Section index:</span></span>  <br/> |<span data-ttu-id="2c732-137">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2c732-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2c732-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2c732-138">Row index:</span></span>  <br/> |<span data-ttu-id="2c732-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="2c732-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="2c732-140">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2c732-140">Cell index:</span></span>  <br/> |<span data-ttu-id="2c732-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="2c732-141">**visSLORelationships**</span></span> <br/> |
   

