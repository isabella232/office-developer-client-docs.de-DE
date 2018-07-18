---
title: Zelle "Value" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798377"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="96669-103">Value Cell (User-Defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="96669-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="96669-104">Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.</span><span class="sxs-lookup"><span data-stu-id="96669-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96669-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96669-105">Remarks</span></span>

<span data-ttu-id="96669-106">Wenn Sie auf diesen Wert in einer anderen Zelle verweisen möchten, geben Sie den in die Zeilenbeschriftung User.Row benutzerdefinierten Namen an.</span><span class="sxs-lookup"><span data-stu-id="96669-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="96669-107">Wenn Sie einen Verweis auf die Zelle Value aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="96669-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96669-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="96669-108">Cell name:</span></span>  <br/> | <span data-ttu-id="96669-109">Benutzer.</span><span class="sxs-lookup"><span data-stu-id="96669-109">User.</span></span>  <span data-ttu-id="96669-110">*Name* . Wert, für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="96669-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="96669-111">*Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="96669-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="96669-112">Wenn Sie einen Verweis auf die Zelle Value aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="96669-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96669-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="96669-113">Section index:</span></span>  <br/> |<span data-ttu-id="96669-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="96669-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="96669-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="96669-115">Row index:</span></span>  <br/> |<span data-ttu-id="96669-116">**VisRowUser** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="96669-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="96669-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="96669-117">Cell index:</span></span>  <br/> |<span data-ttu-id="96669-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="96669-118">**visUserValue**</span></span> <br/> |
   

