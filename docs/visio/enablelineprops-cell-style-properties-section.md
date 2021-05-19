---
title: Zelle "EnableLineProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
ms.openlocfilehash: 38964194626be052b2a168fa929b69ebe4b28e01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410000"
---
# <a name="enablelineprops-cell-style-properties-section"></a><span data-ttu-id="59c1c-103">Zelle "EnableLineProps" (Abschnitt "Style Properties")</span><span class="sxs-lookup"><span data-stu-id="59c1c-103">EnableLineProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="59c1c-104">Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="59c1c-104">Determines whether a style includes line properties.</span></span>
  
|<span data-ttu-id="59c1c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="59c1c-105">**Value**</span></span>|<span data-ttu-id="59c1c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59c1c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59c1c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="59c1c-107">TRUE</span></span>  <br/> |<span data-ttu-id="59c1c-108">Linieneigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="59c1c-108">Include line properties.</span></span>  <br/> |
|<span data-ttu-id="59c1c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="59c1c-109">FALSE</span></span>  <br/> |<span data-ttu-id="59c1c-110">Linieneigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="59c1c-110">Exclude line properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59c1c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59c1c-111">Remarks</span></span>

<span data-ttu-id="59c1c-112">Um einen Verweis auf die Zelle EnableLineProps anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="59c1c-112">To get a reference to the EnableLineProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59c1c-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="59c1c-113">Cell name:</span></span>  <br/> |<span data-ttu-id="59c1c-114">EnableLineProps</span><span class="sxs-lookup"><span data-stu-id="59c1c-114">EnableLineProps</span></span>  <br/> |
   
<span data-ttu-id="59c1c-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EnableLineProps-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="59c1c-115">To get a reference to the EnableLineProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59c1c-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="59c1c-116">Section index:</span></span>  <br/> |<span data-ttu-id="59c1c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59c1c-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="59c1c-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="59c1c-118">Row index:</span></span>  <br/> |<span data-ttu-id="59c1c-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="59c1c-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="59c1c-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="59c1c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="59c1c-121">**visStyleIncludesLine**</span><span class="sxs-lookup"><span data-stu-id="59c1c-121">**visStyleIncludesLine**</span></span> <br/> |
   

