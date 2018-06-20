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
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797388"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="bb727-103">LockPreview Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="bb727-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="bb727-104">Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bb727-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="bb727-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bb727-105">**Value**</span></span>|<span data-ttu-id="bb727-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb727-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bb727-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bb727-107">TRUE</span></span>  <br/> | <span data-ttu-id="bb727-108">Vorschau nicht jedes Mal speichern, wenn eine Zeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bb727-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="bb727-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bb727-109">FALSE</span></span>  <br/> | <span data-ttu-id="bb727-110">Vorschau jedes Mal speichern, wenn eine Zeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bb727-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb727-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb727-111">Remarks</span></span>

<span data-ttu-id="bb727-112">Wenn Sie einen Verweis auf die Zelle LockPreview nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bb727-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb727-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bb727-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bb727-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="bb727-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="bb727-115">Wenn Sie einen Verweis auf die Zelle LockPreview aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bb727-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb727-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bb727-116">Section index:</span></span>  <br/> |<span data-ttu-id="bb727-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bb727-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bb727-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bb727-118">Row index:</span></span>  <br/> |<span data-ttu-id="bb727-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="bb727-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="bb727-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bb727-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bb727-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="bb727-121">**visDocLockPreview**</span></span> <br/> |
   

