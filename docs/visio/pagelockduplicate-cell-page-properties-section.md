---
title: PageLockDuplicate Cell (Page Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Bestimmt, ob die Seite dupliziert werden kann, als boolescher Wert.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283664"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="9eba8-103">PageLockDuplicate Cell (Page Properties section)</span><span class="sxs-lookup"><span data-stu-id="9eba8-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="9eba8-104">Bestimmt, ob die Seite dupliziert werden kann, als boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="9eba8-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9eba8-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="9eba8-105">TRUE</span></span>  <br/> |<span data-ttu-id="9eba8-106">**Duplikate** im Kontextmenü der Seite und die **Page. Duplicate** -Automatisierungsmethode sind beide für die Seite deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9eba8-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="9eba8-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="9eba8-107">FALSE</span></span>  <br/> |<span data-ttu-id="9eba8-108">Die Seite kann dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="9eba8-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9eba8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eba8-109">Remarks</span></span>

<span data-ttu-id="9eba8-110">Wenn Sie einen Verweis auf die Zelle **PageLockDuplicate** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9eba8-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9eba8-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9eba8-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9eba8-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="9eba8-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="9eba8-113">Wenn Sie einen Verweis auf die Zelle **PageLockDuplicate** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9eba8-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9eba8-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9eba8-114">Section index:</span></span>  <br/> |<span data-ttu-id="9eba8-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9eba8-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9eba8-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9eba8-116">Row index:</span></span>  <br/> |<span data-ttu-id="9eba8-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="9eba8-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="9eba8-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9eba8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9eba8-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="9eba8-119">**visPageLockDuplicate**</span></span> <br/> |
   

