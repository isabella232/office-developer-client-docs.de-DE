---
title: Zelle "LockFromGroupFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426058"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="57141-102">Zelle "LockFromGroupFormat" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="57141-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="57141-103">Verhindert, dass Formatänderungen an einem Gruppen-Shape an seine Unterformen verbreitet werden, während benutzer dennoch ausgewählte Unterformen direkt formatieren können.</span><span class="sxs-lookup"><span data-stu-id="57141-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="57141-104">Der Wert der Zelle LockFromGroupFormat  entspricht der Kontrollkästchen Von-Gruppenformatierung im Dialogfeld **Schutz.**</span><span class="sxs-lookup"><span data-stu-id="57141-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="57141-105">Verwenden Sie zum Verweisen auf die Zelle LockFromGroupFormat anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="57141-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57141-106">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="57141-106">Cell name:</span></span>  <br/> |<span data-ttu-id="57141-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="57141-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="57141-108">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um von einem Programm aus auf die Zelle LockFromGroupFormat nach Index zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="57141-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57141-109">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="57141-109">Section index:</span></span>  <br/> |<span data-ttu-id="57141-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="57141-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="57141-111">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="57141-111">Row index:</span></span>  <br/> |<span data-ttu-id="57141-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="57141-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="57141-113">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="57141-113">Cell index:</span></span>  <br/> |<span data-ttu-id="57141-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="57141-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="57141-115">Der Standardwert für diese Zelle ist 0 (False).</span><span class="sxs-lookup"><span data-stu-id="57141-115">The default value for the cell is 0 (False).</span></span>
  

