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
ms.openlocfilehash: a51f83624192615e84292129d4788ae1e2779c6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796929"
---
# <a name="enabletextprops-cell-style-properties-section"></a><span data-ttu-id="4a699-103">EnableTextProps Cell (Style Properties Section)</span><span class="sxs-lookup"><span data-stu-id="4a699-103">EnableTextProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="4a699-104">Bestimmt, ob eine Formatvorlage Texteigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="4a699-104">Determines whether a style includes text properties.</span></span>
  
|<span data-ttu-id="4a699-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4a699-105">**Value**</span></span>|<span data-ttu-id="4a699-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a699-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a699-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4a699-107">TRUE</span></span>  <br/> |<span data-ttu-id="4a699-108">Texteigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="4a699-108">Include text properties.</span></span>  <br/> |
|<span data-ttu-id="4a699-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4a699-109">FALSE</span></span>  <br/> |<span data-ttu-id="4a699-110">Texteigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="4a699-110">Exclude text properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a699-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a699-111">Remarks</span></span>

<span data-ttu-id="4a699-112">Wenn Sie einen Verweis auf die Zelle EnableTextProps aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4a699-112">To get a reference to the EnableTextProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a699-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4a699-113">Cell name:</span></span>  <br/> |<span data-ttu-id="4a699-114">EnableTextProps</span><span class="sxs-lookup"><span data-stu-id="4a699-114">EnableTextProps</span></span>  <br/> |
   
<span data-ttu-id="4a699-115">Wenn Sie einen Verweis auf die Zelle EnableTextProps aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4a699-115">To get a reference to the EnableTextProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a699-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4a699-116">Section index:</span></span>  <br/> |<span data-ttu-id="4a699-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4a699-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4a699-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4a699-118">Row index:</span></span>  <br/> |<span data-ttu-id="4a699-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="4a699-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="4a699-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4a699-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4a699-121">**visStyleIncludesText**</span><span class="sxs-lookup"><span data-stu-id="4a699-121">**visStyleIncludesText**</span></span> <br/> |
   

