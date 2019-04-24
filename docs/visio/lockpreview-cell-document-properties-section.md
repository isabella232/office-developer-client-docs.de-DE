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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348328"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="27af7-103">Zelle "LockPreview" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="27af7-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="27af7-104">Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="27af7-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="27af7-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="27af7-105">**Value**</span></span>|<span data-ttu-id="27af7-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27af7-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="27af7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="27af7-107">TRUE</span></span>  <br/> | <span data-ttu-id="27af7-108">Vorschau nicht jedes Mal speichern, wenn eine Zeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="27af7-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="27af7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="27af7-109">FALSE</span></span>  <br/> | <span data-ttu-id="27af7-110">Vorschau jedes Mal speichern, wenn eine Zeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="27af7-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27af7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27af7-111">Remarks</span></span>

<span data-ttu-id="27af7-112">Wenn Sie einen Verweis auf die Zelle "LockPreview aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="27af7-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27af7-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="27af7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="27af7-114">"LockPreview</span><span class="sxs-lookup"><span data-stu-id="27af7-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="27af7-115">Wenn Sie einen Verweis auf die Zelle "LockPreview aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="27af7-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27af7-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="27af7-116">Section index:</span></span>  <br/> |<span data-ttu-id="27af7-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27af7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27af7-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="27af7-118">Row index:</span></span>  <br/> |<span data-ttu-id="27af7-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="27af7-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="27af7-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="27af7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="27af7-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="27af7-121">**visDocLockPreview**</span></span> <br/> |
   

