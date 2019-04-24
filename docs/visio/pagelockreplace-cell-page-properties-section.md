---
title: PageLockReplace Cell (Page Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Gibt an, ob die Schaltfläche Shape ersetzen für diese Seite deaktiviert werden soll.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339480"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="a6a90-103">PageLockReplace Cell (Page Properties section)</span><span class="sxs-lookup"><span data-stu-id="a6a90-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="a6a90-104">Gibt an, ob die Schaltfläche **Shape ersetzen** für diese Seite deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6a90-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="a6a90-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a6a90-105">**Value**</span></span>|<span data-ttu-id="a6a90-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6a90-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6a90-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a6a90-107">TRUE</span></span>  <br/> |<span data-ttu-id="a6a90-108">Die Schaltfläche **Shape ändern** ist ausgeblendet, wenn diese Seite aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a6a90-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="a6a90-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a6a90-109">FALSE</span></span>  <br/> |<span data-ttu-id="a6a90-110">Die Schaltfläche **Shape ändern** ist von dieser Seite nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6a90-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="a6a90-111">Die Schaltfläche ist möglicherweise noch abgeblendet, wenn: der **DocLockReplace** auf dem **DocumentSheet** auf **true**festgelegt ist; die **LockReplace** -Zelle für die ausgewählte Form ist auf **true**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6a90-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6a90-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6a90-112">Remarks</span></span>

<span data-ttu-id="a6a90-113">Wenn Sie einen Verweis auf die Zelle **PageLockReplace** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6a90-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6a90-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a6a90-114">Cell name:</span></span>  <br/> | <span data-ttu-id="a6a90-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="a6a90-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="a6a90-116">Wenn Sie einen Verweis auf die Zelle **PageLockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a6a90-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6a90-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a6a90-117">Section index:</span></span>  <br/> |<span data-ttu-id="a6a90-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6a90-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a6a90-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a6a90-119">Row index:</span></span>  <br/> |<span data-ttu-id="a6a90-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="a6a90-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="a6a90-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a6a90-121">Cell index:</span></span>  <br/> |<span data-ttu-id="a6a90-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="a6a90-122">**visPageLockReplace**</span></span> <br/> |
   

