---
title: Zelle "EnableTextProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: Bestimmt, ob eine Formatvorlage Texteigenschaften enthält.
ms.openlocfilehash: 3f1d87316955b4e6e40cea16634cff7645a720fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419261"
---
# <a name="enabletextprops-cell-style-properties-section"></a><span data-ttu-id="2e58d-103">Zelle "EnableTextProps" (Abschnitt "Style Properties")</span><span class="sxs-lookup"><span data-stu-id="2e58d-103">EnableTextProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="2e58d-104">Bestimmt, ob eine Formatvorlage Texteigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2e58d-104">Determines whether a style includes text properties.</span></span>
  
|<span data-ttu-id="2e58d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2e58d-105">**Value**</span></span>|<span data-ttu-id="2e58d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e58d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e58d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e58d-107">TRUE</span></span>  <br/> |<span data-ttu-id="2e58d-108">Texteigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="2e58d-108">Include text properties.</span></span>  <br/> |
|<span data-ttu-id="2e58d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e58d-109">FALSE</span></span>  <br/> |<span data-ttu-id="2e58d-110">Texteigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="2e58d-110">Exclude text properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e58d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e58d-111">Remarks</span></span>

<span data-ttu-id="2e58d-112">Um einen Verweis auf die Zelle EnableTextProps anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2e58d-112">To get a reference to the EnableTextProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e58d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2e58d-113">Cell name:</span></span>  <br/> |<span data-ttu-id="2e58d-114">EnableTextProps</span><span class="sxs-lookup"><span data-stu-id="2e58d-114">EnableTextProps</span></span>  <br/> |
   
<span data-ttu-id="2e58d-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle EnableTextProps nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2e58d-115">To get a reference to the EnableTextProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e58d-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2e58d-116">Section index:</span></span>  <br/> |<span data-ttu-id="2e58d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e58d-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2e58d-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2e58d-118">Row index:</span></span>  <br/> |<span data-ttu-id="2e58d-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="2e58d-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="2e58d-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2e58d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2e58d-121">**visStyleIncludesText**</span><span class="sxs-lookup"><span data-stu-id="2e58d-121">**visStyleIncludesText**</span></span> <br/> |
   

