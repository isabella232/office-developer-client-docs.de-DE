---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Bestimmt, ob Seiten im Dokument können, wie ein boolescher Wert dupliziert werden.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796870"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="a2306-103">DocLockDuplicatePage Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="a2306-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="a2306-104">Bestimmt, ob Seiten im Dokument können, wie ein boolescher Wert dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="a2306-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2306-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="a2306-105">TRUE</span></span>  <br/> |<span data-ttu-id="a2306-106">**Doppelte** in das Kontextmenü der Seite und die **Page.Duplicate** Automation-Methode sind beide deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2306-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="a2306-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2306-107">FALSE</span></span>  <br/> |<span data-ttu-id="a2306-108">Die Seite kann dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="a2306-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2306-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2306-109">Remarks</span></span>

<span data-ttu-id="a2306-110">Wenn Sie einen Verweis auf die Zelle **DocLockDuplicatePage** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a2306-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2306-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a2306-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a2306-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="a2306-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="a2306-113">Wenn Sie einen Verweis auf die Zelle **DocLockDuplicatePage** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a2306-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2306-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a2306-114">Section index:</span></span>  <br/> |<span data-ttu-id="a2306-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2306-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a2306-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a2306-116">Row index:</span></span>  <br/> |<span data-ttu-id="a2306-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="a2306-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="a2306-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a2306-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a2306-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="a2306-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

