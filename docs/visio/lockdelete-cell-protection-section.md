---
title: Zelle "LockDelete" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Sperrt das Shape, damit es nicht gelöscht werden kann.
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797374"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="732c0-103">LockDelete Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="732c0-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="732c0-104">Sperrt das Shape, damit es nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="732c0-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="732c0-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="732c0-105">**Value**</span></span>|<span data-ttu-id="732c0-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="732c0-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="732c0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="732c0-107">TRUE</span></span>  <br/> | <span data-ttu-id="732c0-108">Shape kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="732c0-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="732c0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="732c0-109">FALSE</span></span>  <br/> | <span data-ttu-id="732c0-110">Shape kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="732c0-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="732c0-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="732c0-111">Remarks</span></span>

<span data-ttu-id="732c0-112">Wenn Sie einen Verweis auf die Zelle LockDelete nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="732c0-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="732c0-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="732c0-113">Cell name:</span></span>  <br/> | <span data-ttu-id="732c0-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="732c0-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="732c0-115">Wenn Sie einen Verweis auf die Zelle LockDelete aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="732c0-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="732c0-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="732c0-116">Section index:</span></span>  <br/> |<span data-ttu-id="732c0-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="732c0-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="732c0-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="732c0-118">Row index:</span></span>  <br/> |<span data-ttu-id="732c0-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="732c0-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="732c0-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="732c0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="732c0-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="732c0-121">**visLockDelete**</span></span> <br/> |
   

