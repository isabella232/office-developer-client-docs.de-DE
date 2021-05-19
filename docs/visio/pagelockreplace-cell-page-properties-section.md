---
title: Zelle "PageLockReplace" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Gibt an, ob die Schaltfläche Shape ersetzen für diese Seite deaktiviert werden soll.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433101"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="b9174-103">Zelle "PageLockReplace" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="b9174-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="b9174-104">Gibt an, **ob** die Schaltfläche Shape ersetzen für diese Seite deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9174-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="b9174-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b9174-105">**Value**</span></span>|<span data-ttu-id="b9174-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9174-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9174-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b9174-107">TRUE</span></span>  <br/> |<span data-ttu-id="b9174-108">Die **Schaltfläche Shape ändern** ist ausgegraut, wenn diese Seite aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="b9174-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="b9174-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b9174-109">FALSE</span></span>  <br/> |<span data-ttu-id="b9174-110">Die **Schaltfläche Shape ändern** wird von dieser Seite nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9174-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="b9174-111">Die Schaltfläche ist möglicherweise noch abgeblendet, wenn: **DocLockReplace** im **DocumentSheet** auf **TRUE festgelegt ist;** Die **Zelle LockReplace** für die ausgewählte Form ist auf **TRUE festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="b9174-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9174-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9174-112">Remarks</span></span>

<span data-ttu-id="b9174-113">Um einen Verweis auf die **Zelle PageLockReplace** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b9174-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9174-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b9174-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b9174-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="b9174-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="b9174-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **PageLockReplace-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b9174-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9174-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b9174-117">Section index:</span></span>  <br/> |<span data-ttu-id="b9174-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b9174-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b9174-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b9174-119">Row index:</span></span>  <br/> |<span data-ttu-id="b9174-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="b9174-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="b9174-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b9174-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b9174-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="b9174-122">**visPageLockReplace**</span></span> <br/> |
   

