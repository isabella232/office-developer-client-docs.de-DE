---
title: Zelle "LockFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Sperrt die Formatierung eines Shapes, damit dieses nicht geändert werden kann.
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797376"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="f8518-103">Zelle "LockFormat" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="f8518-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="f8518-104">Sperrt die Formatierung eines Shapes, damit dieses nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8518-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="f8518-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f8518-105">**Value**</span></span>|<span data-ttu-id="f8518-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8518-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f8518-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f8518-107">TRUE</span></span>  <br/> | <span data-ttu-id="f8518-108">Formatierung kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f8518-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="f8518-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f8518-109">FALSE</span></span>  <br/> | <span data-ttu-id="f8518-110">Formatierung kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f8518-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8518-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8518-111">Remarks</span></span>

<span data-ttu-id="f8518-112">Wenn Sie einen Verweis auf die Zelle LockFormat nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f8518-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8518-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f8518-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f8518-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="f8518-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="f8518-115">Wenn Sie einen Verweis auf die Zelle LockFormat aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f8518-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8518-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f8518-116">Section index:</span></span>  <br/> |<span data-ttu-id="f8518-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8518-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8518-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f8518-118">Row index:</span></span>  <br/> |<span data-ttu-id="f8518-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f8518-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f8518-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f8518-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f8518-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="f8518-121">**visLockFormat**</span></span> <br/> |
   

