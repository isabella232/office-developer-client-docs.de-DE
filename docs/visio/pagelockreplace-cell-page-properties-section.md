---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Gibt an, ob für diese Seite die Schaltfläche Form ersetzen deaktiviert werden soll.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797587"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="e80b0-103">PageLockReplace Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="e80b0-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="e80b0-104">Gibt an, ob für diese Seite die Schaltfläche **Form ersetzen** deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e80b0-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="e80b0-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e80b0-105">**Value**</span></span>|<span data-ttu-id="e80b0-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e80b0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e80b0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e80b0-107">TRUE</span></span>  <br/> |<span data-ttu-id="e80b0-108">Die **Form ändern** -Schaltfläche ist nicht verfügbar, wenn diese Seite aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e80b0-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="e80b0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e80b0-109">FALSE</span></span>  <br/> |<span data-ttu-id="e80b0-110">Auf dieser Seite wird nicht die Schaltfläche **Form ändern** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e80b0-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="e80b0-111">Die Schaltfläche kann weiterhin ausgeführt, wenn abgeblendet werden: die **DocLockReplace** auf die **DocumentSheet** auf **TRUE**; festgelegt ist die Zelle **LockReplace** für das ausgewählte Shape wird auf **TRUE**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e80b0-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e80b0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e80b0-112">Remarks</span></span>

<span data-ttu-id="e80b0-113">Wenn Sie einen Verweis auf die Zelle **PageLockReplace** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e80b0-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e80b0-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e80b0-114">Cell name:</span></span>  <br/> | <span data-ttu-id="e80b0-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="e80b0-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="e80b0-116">Wenn Sie einen Verweis auf die Zelle **PageLockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e80b0-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e80b0-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e80b0-117">Section index:</span></span>  <br/> |<span data-ttu-id="e80b0-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e80b0-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e80b0-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e80b0-119">Row index:</span></span>  <br/> |<span data-ttu-id="e80b0-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e80b0-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="e80b0-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e80b0-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e80b0-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="e80b0-122">**visPageLockReplace**</span></span> <br/> |
   

