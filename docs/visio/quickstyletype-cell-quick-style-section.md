---
title: QuickStyleType Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), die von der Form erbt.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410504"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="54aea-103">QuickStyleType Cell (Quick Style section)</span><span class="sxs-lookup"><span data-stu-id="54aea-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="54aea-104">Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), die von der Form erbt.</span><span class="sxs-lookup"><span data-stu-id="54aea-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="54aea-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="54aea-105">**Value**</span></span>|<span data-ttu-id="54aea-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54aea-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54aea-107">0</span><span class="sxs-lookup"><span data-stu-id="54aea-107">0</span></span>  <br/> |<span data-ttu-id="54aea-108">Visio wählt automatisch</span><span class="sxs-lookup"><span data-stu-id="54aea-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="54aea-109">1</span><span class="sxs-lookup"><span data-stu-id="54aea-109">1</span></span>  <br/> |<span data-ttu-id="54aea-110">1-dimensional</span><span class="sxs-lookup"><span data-stu-id="54aea-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="54aea-111">2</span><span class="sxs-lookup"><span data-stu-id="54aea-111">2</span></span>  <br/> |<span data-ttu-id="54aea-112">2-dimensional</span><span class="sxs-lookup"><span data-stu-id="54aea-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="54aea-113">3</span><span class="sxs-lookup"><span data-stu-id="54aea-113">3</span></span>  <br/> |<span data-ttu-id="54aea-114">Connector</span><span class="sxs-lookup"><span data-stu-id="54aea-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54aea-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54aea-115">Remarks</span></span>

<span data-ttu-id="54aea-116">Wenn Sie einen Verweis auf die Zelle **QuickStyleType** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="54aea-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54aea-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="54aea-117">Cell name:</span></span>  <br/> | <span data-ttu-id="54aea-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="54aea-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="54aea-119">Wenn Sie einen Verweis auf die Zelle **QuickStyleType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="54aea-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54aea-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="54aea-120">Section index:</span></span>  <br/> |<span data-ttu-id="54aea-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54aea-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54aea-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="54aea-122">Row index:</span></span>  <br/> |<span data-ttu-id="54aea-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="54aea-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="54aea-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="54aea-124">Cell index:</span></span>  <br/> |<span data-ttu-id="54aea-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="54aea-125">**visQuickStyleType**</span></span> <br/> |
   

