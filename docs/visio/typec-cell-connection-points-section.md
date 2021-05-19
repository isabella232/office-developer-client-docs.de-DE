---
title: Zelle "Type / C" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Legt den Verbindungspunkttyp fest.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415236"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="e0392-103">Zelle "Type / C" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="e0392-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="e0392-104">Legt den Verbindungspunkttyp fest.</span><span class="sxs-lookup"><span data-stu-id="e0392-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="e0392-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e0392-105">**Value**</span></span>|<span data-ttu-id="e0392-106">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e0392-106">**Type**</span></span>|<span data-ttu-id="e0392-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="e0392-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0392-108">0</span><span class="sxs-lookup"><span data-stu-id="e0392-108">0</span></span>  <br/> |<span data-ttu-id="e0392-109">Nach innen</span><span class="sxs-lookup"><span data-stu-id="e0392-109">Inward</span></span>  <br/> |<span data-ttu-id="e0392-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="e0392-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="e0392-111">1</span><span class="sxs-lookup"><span data-stu-id="e0392-111">1</span></span>  <br/> |<span data-ttu-id="e0392-112">Nach außen</span><span class="sxs-lookup"><span data-stu-id="e0392-112">Outward</span></span>  <br/> |<span data-ttu-id="e0392-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="e0392-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="e0392-114">2</span><span class="sxs-lookup"><span data-stu-id="e0392-114">2</span></span>  <br/> |<span data-ttu-id="e0392-115">Nach innen &amp; nach außen</span><span class="sxs-lookup"><span data-stu-id="e0392-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="e0392-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="e0392-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0392-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0392-117">Remarks</span></span>

<span data-ttu-id="e0392-p101">Sie können den Verbindungspunkttyp auch festlegen, indem Sie das Tool **Automatischer Verbinder** sowie ein Shape auswählen und anschließend mit der rechten Maustaste auf einen Verbindungspunkt klicken. Dazu müssen Sie in den [Entwicklermodus](run-in-developer-mode-display-the-developer-tab.md) wechseln.</span><span class="sxs-lookup"><span data-stu-id="e0392-p101">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point. To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="e0392-120">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Type /C anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="e0392-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0392-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e0392-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e0392-122">Connections.Type[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e0392-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e0392-123">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Type /C nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e0392-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0392-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e0392-124">Section index:</span></span>  <br/> |<span data-ttu-id="e0392-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="e0392-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="e0392-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e0392-126">Row index:</span></span>  <br/> |<span data-ttu-id="e0392-127">**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e0392-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e0392-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e0392-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e0392-129">**visCnnctType** (nicht erweiterte Zeilen) **visCnnctC** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="e0392-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="e0392-130">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="e0392-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

