---
title: Zelle "PageLockDuplicate" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Bestimmt, ob die Seite als boolescher Wert dupliziert werden kann.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425981"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="e3203-103">Zelle "PageLockDuplicate" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="e3203-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="e3203-104">Bestimmt, ob die Seite als boolescher Wert dupliziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3203-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3203-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="e3203-105">TRUE</span></span>  <br/> |<span data-ttu-id="e3203-106">**Duplikate** im Kontextmenü der Seite und die **Page.Duplicate-Automatisierungsmethode** sind beide für die Seite deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e3203-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="e3203-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="e3203-107">FALSE</span></span>  <br/> |<span data-ttu-id="e3203-108">Die Seite kann dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="e3203-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3203-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3203-109">Remarks</span></span>

<span data-ttu-id="e3203-110">Um einen Verweis auf die **Zelle PageLockDuplicate** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="e3203-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3203-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e3203-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e3203-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="e3203-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="e3203-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **PageLockDuplicate-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e3203-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3203-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e3203-114">Section index:</span></span>  <br/> |<span data-ttu-id="e3203-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3203-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e3203-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e3203-116">Row index:</span></span>  <br/> |<span data-ttu-id="e3203-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e3203-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="e3203-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e3203-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e3203-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="e3203-119">**visPageLockDuplicate**</span></span> <br/> |
   

