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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328917"
---
# <a name="enabletextprops-cell-style-properties-section"></a><span data-ttu-id="ab0dc-103">Zelle "EnableTextProps" (Abschnitt "Style Properties")</span><span class="sxs-lookup"><span data-stu-id="ab0dc-103">EnableTextProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="ab0dc-104">Bestimmt, ob eine Formatvorlage Texteigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ab0dc-104">Determines whether a style includes text properties.</span></span>
  
|<span data-ttu-id="ab0dc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ab0dc-105">**Value**</span></span>|<span data-ttu-id="ab0dc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab0dc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab0dc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ab0dc-107">TRUE</span></span>  <br/> |<span data-ttu-id="ab0dc-108">Texteigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="ab0dc-108">Include text properties.</span></span>  <br/> |
|<span data-ttu-id="ab0dc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ab0dc-109">FALSE</span></span>  <br/> |<span data-ttu-id="ab0dc-110">Texteigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="ab0dc-110">Exclude text properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab0dc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab0dc-111">Remarks</span></span>

<span data-ttu-id="ab0dc-112">Wenn Sie einen Verweis auf die Zelle "EnableTextProps aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ab0dc-112">To get a reference to the EnableTextProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab0dc-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ab0dc-113">Cell name:</span></span>  <br/> |<span data-ttu-id="ab0dc-114">"EnableTextProps</span><span class="sxs-lookup"><span data-stu-id="ab0dc-114">EnableTextProps</span></span>  <br/> |
   
<span data-ttu-id="ab0dc-115">Wenn Sie einen Verweis auf die Zelle "EnableTextProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ab0dc-115">To get a reference to the EnableTextProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab0dc-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ab0dc-116">Section index:</span></span>  <br/> |<span data-ttu-id="ab0dc-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ab0dc-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ab0dc-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ab0dc-118">Row index:</span></span>  <br/> |<span data-ttu-id="ab0dc-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="ab0dc-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="ab0dc-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ab0dc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ab0dc-121">**visStyleIncludesText**</span><span class="sxs-lookup"><span data-stu-id="ab0dc-121">**visStyleIncludesText**</span></span> <br/> |
   

