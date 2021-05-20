---
title: Zelle "DocLockDuplicatePage" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Bestimmt, ob Seiten im Dokument als Boolean dupliziert werden können.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439660"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="eca81-103">Zelle "DocLockDuplicatePage" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="eca81-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="eca81-104">Bestimmt, ob Seiten im Dokument als Boolean dupliziert werden können.</span><span class="sxs-lookup"><span data-stu-id="eca81-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eca81-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="eca81-105">TRUE</span></span>  <br/> |<span data-ttu-id="eca81-106">**Duplikate** im Kontextmenü der Seite und die **Page.Duplicate-Automatisierungsmethode** sind beide deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eca81-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="eca81-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="eca81-107">FALSE</span></span>  <br/> |<span data-ttu-id="eca81-108">Die Seite kann dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="eca81-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eca81-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eca81-109">Remarks</span></span>

<span data-ttu-id="eca81-110">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle DocLockDuplicatePage** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="eca81-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eca81-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="eca81-111">Cell name:</span></span>  <br/> | <span data-ttu-id="eca81-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="eca81-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="eca81-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **DocLockDuplicatePage-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="eca81-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eca81-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="eca81-114">Section index:</span></span>  <br/> |<span data-ttu-id="eca81-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eca81-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eca81-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="eca81-116">Row index:</span></span>  <br/> |<span data-ttu-id="eca81-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="eca81-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="eca81-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="eca81-118">Cell index:</span></span>  <br/> |<span data-ttu-id="eca81-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="eca81-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

