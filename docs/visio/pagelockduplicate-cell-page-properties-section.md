---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Bestimmt, ob die Seite kann, wie ein boolescher Wert dupliziert werden.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797581"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="88fcb-103">PageLockDuplicate Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="88fcb-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="88fcb-104">Bestimmt, ob die Seite kann, wie ein boolescher Wert dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="88fcb-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88fcb-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="88fcb-105">TRUE</span></span>  <br/> |<span data-ttu-id="88fcb-106">**Doppelte** in das Kontextmenü der Seite und die **Page.Duplicate** Automation-Methode sind beide deaktiviert für die Seite.</span><span class="sxs-lookup"><span data-stu-id="88fcb-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="88fcb-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="88fcb-107">FALSE</span></span>  <br/> |<span data-ttu-id="88fcb-108">Die Seite kann dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="88fcb-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88fcb-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88fcb-109">Remarks</span></span>

<span data-ttu-id="88fcb-110">Wenn Sie einen Verweis auf die Zelle **PageLockDuplicate** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="88fcb-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88fcb-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="88fcb-111">Cell name:</span></span>  <br/> | <span data-ttu-id="88fcb-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="88fcb-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="88fcb-113">Wenn Sie einen Verweis auf die Zelle **PageLockDuplicate** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="88fcb-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88fcb-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="88fcb-114">Section index:</span></span>  <br/> |<span data-ttu-id="88fcb-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="88fcb-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="88fcb-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="88fcb-116">Row index:</span></span>  <br/> |<span data-ttu-id="88fcb-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="88fcb-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="88fcb-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="88fcb-118">Cell index:</span></span>  <br/> |<span data-ttu-id="88fcb-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="88fcb-119">**visPageLockDuplicate**</span></span> <br/> |
   

