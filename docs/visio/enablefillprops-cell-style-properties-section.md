---
title: Zelle "EnableFillProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.
ms.openlocfilehash: 399af4b9d1a2245ea7a9b91ebbf036eb122f15bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796935"
---
# <a name="enablefillprops-cell-style-properties-section"></a><span data-ttu-id="97b36-103">EnableFillProps Cell (Style Properties Section)</span><span class="sxs-lookup"><span data-stu-id="97b36-103">EnableFillProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="97b36-104">Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="97b36-104">Determines whether a style includes fill properties.</span></span>
  
|<span data-ttu-id="97b36-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="97b36-105">**Value**</span></span>|<span data-ttu-id="97b36-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97b36-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97b36-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="97b36-107">TRUE</span></span>  <br/> |<span data-ttu-id="97b36-108">Füllbereichseigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="97b36-108">Include fill properties.</span></span>  <br/> |
|<span data-ttu-id="97b36-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="97b36-109">FALSE</span></span>  <br/> |<span data-ttu-id="97b36-110">Füllbereichseigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="97b36-110">Exclude fill properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97b36-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97b36-111">Remarks</span></span>

<span data-ttu-id="97b36-112">Wenn Sie einen Verweis auf die Zelle EnableFillProps nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97b36-112">To get a reference to the EnableFillProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97b36-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="97b36-113">Cell name:</span></span>  <br/> |<span data-ttu-id="97b36-114">EnableFillProps</span><span class="sxs-lookup"><span data-stu-id="97b36-114">EnableFillProps</span></span>  <br/> |
   
<span data-ttu-id="97b36-115">Wenn Sie einen Verweis auf die Zelle EnableFillProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="97b36-115">To get a reference to the EnableFillProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97b36-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="97b36-116">Section index:</span></span>  <br/> |<span data-ttu-id="97b36-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97b36-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="97b36-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="97b36-118">Row index:</span></span>  <br/> |<span data-ttu-id="97b36-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="97b36-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="97b36-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="97b36-120">Cell index:</span></span>  <br/> |<span data-ttu-id="97b36-121">**visStyleIncludesFill**</span><span class="sxs-lookup"><span data-stu-id="97b36-121">**visStyleIncludesFill**</span></span> <br/> |
   

