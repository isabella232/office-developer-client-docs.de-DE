---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Bestimmt, ob die Form ersetzen Benutzeroberfläche für dieses Dokument deaktiviert werden soll.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796894"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="f5df3-103">DocLockReplace Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="f5df3-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="f5df3-104">Bestimmt, ob die Form ersetzen Benutzeroberfläche für dieses Dokument deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5df3-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5df3-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="f5df3-105">TRUE</span></span>  <br/> |<span data-ttu-id="f5df3-106">Die **Form ersetzen** -Schaltfläche ist nicht in der Benutzeroberfläche verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5df3-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="f5df3-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="f5df3-107">FALSE</span></span>  <br/> |<span data-ttu-id="f5df3-108">Die **Form ersetzen** -Schaltfläche ist aktiv in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f5df3-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="f5df3-109">Benutzer können das Feature Shapes ersetzen Sie in diesem Dokument verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5df3-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5df3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5df3-110">Remarks</span></span>

<span data-ttu-id="f5df3-111">Wenn Sie einen Verweis auf die Zelle **DocLockReplace** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f5df3-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5df3-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f5df3-112">Cell name:</span></span>  <br/> | <span data-ttu-id="f5df3-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="f5df3-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="f5df3-114">Wenn Sie einen Verweis auf die Zelle **DocLocReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f5df3-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5df3-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f5df3-115">Section index:</span></span>  <br/> |<span data-ttu-id="f5df3-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f5df3-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f5df3-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f5df3-117">Row index:</span></span>  <br/> |<span data-ttu-id="f5df3-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="f5df3-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="f5df3-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f5df3-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f5df3-120">** VisDocLockReplace **</span><span class="sxs-lookup"><span data-stu-id="f5df3-120">**visDocLockReplace **</span></span> <br/> |
   

