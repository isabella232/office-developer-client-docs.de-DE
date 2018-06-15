---
title: Zelle "LockSelect" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Verhindert, dass ein Shape ausgewählt werden kann.
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797403"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="8297c-103">Zelle "LockSelect" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="8297c-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="8297c-104">Verhindert, dass ein Shape ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8297c-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="8297c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8297c-105">**Value**</span></span>|<span data-ttu-id="8297c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8297c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8297c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8297c-107">TRUE</span></span>  <br/> | <span data-ttu-id="8297c-108">Shape kann nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="8297c-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="8297c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8297c-109">FALSE</span></span>  <br/> | <span data-ttu-id="8297c-110">Shape kann ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="8297c-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8297c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8297c-111">Remarks</span></span>

<span data-ttu-id="8297c-112">In Damit LockSelect wirksam wird muss das Kontrollkästchen **Shapes** im Dialogfeld **Dokument schützen** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="8297c-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="8297c-113">Wenn Sie einen Verweis auf die Zelle LockSelect nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8297c-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8297c-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8297c-114">Cell name:</span></span>  <br/> | <span data-ttu-id="8297c-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="8297c-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="8297c-116">Wenn Sie einen Verweis auf die Zelle LockSelect aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8297c-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8297c-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8297c-117">Section index:</span></span>  <br/> |<span data-ttu-id="8297c-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8297c-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8297c-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8297c-119">Row index:</span></span>  <br/> |<span data-ttu-id="8297c-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8297c-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8297c-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8297c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="8297c-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="8297c-122">**visLockSelect**</span></span> <br/> |
   

