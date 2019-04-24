---
title: DocLockReplace Cell (Document Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Bestimmt, ob die Benutzeroberfläche für das Ersetzen für dieses Dokument deaktiviert werden soll.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338605"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="b8d3d-103">DocLockReplace Cell (Document Properties section)</span><span class="sxs-lookup"><span data-stu-id="b8d3d-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="b8d3d-104">Bestimmt, ob die Benutzeroberfläche für das Ersetzen für dieses Dokument deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8d3d-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="b8d3d-105">TRUE</span></span>  <br/> |<span data-ttu-id="b8d3d-106">Die Schaltfläche **Shape ersetzen** ist auf der Benutzeroberfläche abgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="b8d3d-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="b8d3d-107">FALSE</span></span>  <br/> |<span data-ttu-id="b8d3d-108">Die Schaltfläche **Shape ersetzen** ist auf der Benutzeroberfläche aktiv.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="b8d3d-109">Benutzer können die Funktion Shape ersetzen in diesem Dokument verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8d3d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8d3d-110">Remarks</span></span>

<span data-ttu-id="b8d3d-111">Wenn Sie einen Verweis auf die Zelle **DocLockReplace** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8d3d-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-112">Cell name:</span></span>  <br/> | <span data-ttu-id="b8d3d-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="b8d3d-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="b8d3d-114">Wenn Sie einen Verweis auf die Zelle **DocLocReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8d3d-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-115">Section index:</span></span>  <br/> |<span data-ttu-id="b8d3d-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b8d3d-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b8d3d-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-117">Row index:</span></span>  <br/> |<span data-ttu-id="b8d3d-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="b8d3d-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="b8d3d-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b8d3d-120">\* \* visDocLockReplace \* \*</span><span class="sxs-lookup"><span data-stu-id="b8d3d-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

