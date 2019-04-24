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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329106"
---
# <a name="enablelineprops-cell-style-properties-section"></a><span data-ttu-id="fdbbf-103">Zelle "EnableLineProps" (Abschnitt "Style Properties")</span><span class="sxs-lookup"><span data-stu-id="fdbbf-103">EnableLineProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="fdbbf-104">Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="fdbbf-104">Determines whether a style includes line properties.</span></span>
  
|<span data-ttu-id="fdbbf-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fdbbf-105">**Value**</span></span>|<span data-ttu-id="fdbbf-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fdbbf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fdbbf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fdbbf-107">TRUE</span></span>  <br/> |<span data-ttu-id="fdbbf-108">Linieneigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="fdbbf-108">Include line properties.</span></span>  <br/> |
|<span data-ttu-id="fdbbf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fdbbf-109">FALSE</span></span>  <br/> |<span data-ttu-id="fdbbf-110">Linieneigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="fdbbf-110">Exclude line properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdbbf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdbbf-111">Remarks</span></span>

<span data-ttu-id="fdbbf-112">Wenn Sie einen Verweis auf die Zelle "EnableLineProps aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdbbf-112">To get a reference to the EnableLineProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fdbbf-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fdbbf-113">Cell name:</span></span>  <br/> |<span data-ttu-id="fdbbf-114">"EnableLineProps</span><span class="sxs-lookup"><span data-stu-id="fdbbf-114">EnableLineProps</span></span>  <br/> |
   
<span data-ttu-id="fdbbf-115">Wenn Sie einen Verweis auf die Zelle "EnableLineProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="fdbbf-115">To get a reference to the EnableLineProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fdbbf-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fdbbf-116">Section index:</span></span>  <br/> |<span data-ttu-id="fdbbf-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fdbbf-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fdbbf-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fdbbf-118">Row index:</span></span>  <br/> |<span data-ttu-id="fdbbf-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="fdbbf-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="fdbbf-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fdbbf-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fdbbf-121">**visStyleIncludesLine**</span><span class="sxs-lookup"><span data-stu-id="fdbbf-121">**visStyleIncludesLine**</span></span> <br/> |
   

