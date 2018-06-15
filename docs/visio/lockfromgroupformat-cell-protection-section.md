---
title: Zelle "LockFromGroupFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797391"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="e75ed-102">LockFromGroupFormat Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="e75ed-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="e75ed-103">Blöcke format, Änderungen in einem Gruppen-Shape aus, die Teil-Shapes weitergegeben wird, während Benutzer dennoch ausgewählten untergeordneten Shapes direkt zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="e75ed-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="e75ed-104">Der Wert der Zelle LockFromGroupFormat entspricht der Einstellung für das Kontrollkästchen **von gruppenformatierung** im Dialogfeld **Schutz** .</span><span class="sxs-lookup"><span data-stu-id="e75ed-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="e75ed-105">Auf die Zelle LockFromGroupFormat aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen verweisen verwenden:</span><span class="sxs-lookup"><span data-stu-id="e75ed-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e75ed-106">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e75ed-106">Cell name:</span></span>  <br/> |<span data-ttu-id="e75ed-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="e75ed-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="e75ed-108">Wenn Sie auf die Zelle LockFromGroupFormat durch Index aus einem Programm verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e75ed-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e75ed-109">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e75ed-109">Section index:</span></span>  <br/> |<span data-ttu-id="e75ed-110">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e75ed-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e75ed-111">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e75ed-111">Row index:</span></span>  <br/> |<span data-ttu-id="e75ed-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e75ed-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="e75ed-113">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e75ed-113">Cell index:</span></span>  <br/> |<span data-ttu-id="e75ed-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="e75ed-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="e75ed-115">Der Standardwert für diese Zelle ist 0 (False).</span><span class="sxs-lookup"><span data-stu-id="e75ed-115">The default value for the cell is 0 (False).</span></span>
  

