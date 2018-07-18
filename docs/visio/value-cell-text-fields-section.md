---
title: Zelle "Value" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Enthält die Funktion für ein Feld.
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798372"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="9b835-103">Value Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="9b835-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="9b835-104">Enthält die Funktion für ein Feld.</span><span class="sxs-lookup"><span data-stu-id="9b835-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b835-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b835-105">Remarks</span></span>

<span data-ttu-id="9b835-106">Sie können den Wert dieser Zelle im Dialogfeld **Feld** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld**).</span><span class="sxs-lookup"><span data-stu-id="9b835-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="9b835-107">Wenn Sie einen Verweis auf die Zelle Value aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9b835-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b835-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9b835-108">Cell name:</span></span>  <br/> |<span data-ttu-id="9b835-109">Fields.Value [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9b835-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9b835-110">Wenn Sie einen Verweis auf die Zelle Value aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9b835-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b835-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9b835-111">Section index:</span></span>  <br/> |<span data-ttu-id="9b835-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="9b835-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="9b835-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9b835-113">Row index:</span></span>  <br/> |<span data-ttu-id="9b835-114">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9b835-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9b835-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9b835-115">Cell index:</span></span>  <br/> |<span data-ttu-id="9b835-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="9b835-116">**visFieldCell**</span></span> <br/> |
   

