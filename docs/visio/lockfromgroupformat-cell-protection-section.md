---
title: Zelle "LockFromGroupFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359591"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="da569-102">Zelle "LockFromGroupFormat" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="da569-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="da569-103">Blockiert Formatänderungen an einem Gruppen-Shape, die an die unter Formen weitergegeben werden, während Benutzer die ausgewählten unter Formen weiterhin direkt formatieren können.</span><span class="sxs-lookup"><span data-stu-id="da569-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="da569-104">Der Wert der Zelle LockFromGroupFormat entspricht dem Kontrollkästchen **von Gruppen Formatierungen** im Dialogfeld **Schutz** .</span><span class="sxs-lookup"><span data-stu-id="da569-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="da569-105">Wenn Sie auf die Zelle LockFromGroupFormat aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen verweisen möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="da569-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da569-106">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="da569-106">Cell name:</span></span>  <br/> |<span data-ttu-id="da569-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="da569-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="da569-108">Wenn Sie aus einem Programm aus nach Index auf die Zelle LockFromGroupFormat verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="da569-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da569-109">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="da569-109">Section index:</span></span>  <br/> |<span data-ttu-id="da569-110">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="da569-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="da569-111">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="da569-111">Row index:</span></span>  <br/> |<span data-ttu-id="da569-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="da569-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="da569-113">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="da569-113">Cell index:</span></span>  <br/> |<span data-ttu-id="da569-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="da569-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="da569-115">Der Standardwert für diese Zelle ist 0 (False).</span><span class="sxs-lookup"><span data-stu-id="da569-115">The default value for the cell is 0 (False).</span></span>
  

