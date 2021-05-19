---
title: Zelle "LockPreview" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418862"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="36ca5-103">Zelle "LockPreview" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="36ca5-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="36ca5-104">Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="36ca5-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="36ca5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="36ca5-105">**Value**</span></span>|<span data-ttu-id="36ca5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36ca5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36ca5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="36ca5-107">TRUE</span></span>  <br/> | <span data-ttu-id="36ca5-108">Vorschau nicht jedes Mal speichern, wenn eine Zeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="36ca5-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="36ca5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="36ca5-109">FALSE</span></span>  <br/> | <span data-ttu-id="36ca5-110">Vorschau jedes Mal speichern, wenn eine Zeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="36ca5-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36ca5-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36ca5-111">Remarks</span></span>

<span data-ttu-id="36ca5-112">Um einen Verweis auf die Zelle LockPreview anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="36ca5-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="36ca5-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="36ca5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="36ca5-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="36ca5-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="36ca5-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockPreview nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="36ca5-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="36ca5-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="36ca5-116">Section index:</span></span>  <br/> |<span data-ttu-id="36ca5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36ca5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="36ca5-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="36ca5-118">Row index:</span></span>  <br/> |<span data-ttu-id="36ca5-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="36ca5-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="36ca5-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="36ca5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="36ca5-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="36ca5-121">**visDocLockPreview**</span></span> <br/> |
   

