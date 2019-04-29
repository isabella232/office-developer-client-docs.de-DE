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
ms.openlocfilehash: 55191cb28d5777f7fb65a3a1e4be890e6dda4e8b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406010"
---
# <a name="enablefillprops-cell-style-properties-section"></a><span data-ttu-id="8e844-103">Zelle "EnableFillProps" (Abschnitt "Style Properties")</span><span class="sxs-lookup"><span data-stu-id="8e844-103">EnableFillProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="8e844-104">Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="8e844-104">Determines whether a style includes fill properties.</span></span>
  
|<span data-ttu-id="8e844-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8e844-105">**Value**</span></span>|<span data-ttu-id="8e844-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e844-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e844-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8e844-107">TRUE</span></span>  <br/> |<span data-ttu-id="8e844-108">Füllbereichseigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="8e844-108">Include fill properties.</span></span>  <br/> |
|<span data-ttu-id="8e844-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8e844-109">FALSE</span></span>  <br/> |<span data-ttu-id="8e844-110">Füllbereichseigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="8e844-110">Exclude fill properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e844-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e844-111">Remarks</span></span>

<span data-ttu-id="8e844-112">Wenn Sie einen Verweis auf die Zelle "EnableFillProps aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8e844-112">To get a reference to the EnableFillProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e844-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8e844-113">Cell name:</span></span>  <br/> |<span data-ttu-id="8e844-114">"EnableFillProps</span><span class="sxs-lookup"><span data-stu-id="8e844-114">EnableFillProps</span></span>  <br/> |
   
<span data-ttu-id="8e844-115">Wenn Sie einen Verweis auf die Zelle "EnableFillProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8e844-115">To get a reference to the EnableFillProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e844-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8e844-116">Section index:</span></span>  <br/> |<span data-ttu-id="8e844-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e844-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8e844-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8e844-118">Row index:</span></span>  <br/> |<span data-ttu-id="8e844-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="8e844-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="8e844-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8e844-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8e844-121">**visStyleIncludesFill**</span><span class="sxs-lookup"><span data-stu-id="8e844-121">**visStyleIncludesFill**</span></span> <br/> |
   

