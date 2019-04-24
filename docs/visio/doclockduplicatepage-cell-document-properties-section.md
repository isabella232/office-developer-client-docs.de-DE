---
title: DocLockDuplicatePage Cell (Document Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Bestimmt, ob Seiten im Dokument als boolescher Wert dupliziert werden können.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338542"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="09243-103">DocLockDuplicatePage Cell (Document Properties section)</span><span class="sxs-lookup"><span data-stu-id="09243-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="09243-104">Bestimmt, ob Seiten im Dokument als boolescher Wert dupliziert werden können.</span><span class="sxs-lookup"><span data-stu-id="09243-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09243-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="09243-105">TRUE</span></span>  <br/> |<span data-ttu-id="09243-106">**Duplikate** im Kontextmenü der Seite und die **Page. Duplicate** -Automatisierungsmethode sind beide deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="09243-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="09243-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="09243-107">FALSE</span></span>  <br/> |<span data-ttu-id="09243-108">Die Seite kann dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="09243-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09243-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09243-109">Remarks</span></span>

<span data-ttu-id="09243-110">Wenn Sie einen Verweis auf die Zelle **DocLockDuplicatePage** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="09243-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09243-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="09243-111">Cell name:</span></span>  <br/> | <span data-ttu-id="09243-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="09243-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="09243-113">Wenn Sie einen Verweis auf die Zelle **DocLockDuplicatePage** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="09243-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09243-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="09243-114">Section index:</span></span>  <br/> |<span data-ttu-id="09243-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="09243-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="09243-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="09243-116">Row index:</span></span>  <br/> |<span data-ttu-id="09243-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="09243-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="09243-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="09243-118">Cell index:</span></span>  <br/> |<span data-ttu-id="09243-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="09243-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

