---
title: Zelle "UICode" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Bestimmt den Code eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327343"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="75465-103">Zelle "UICode" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="75465-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="75465-104">Bestimmt den Code eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="75465-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75465-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75465-105">Remarks</span></span>

<span data-ttu-id="75465-p101">Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie diese Zelle, wenn es um die Abwärtskompatibilität geht, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="75465-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="75465-108">Wenn Sie einen Verweis auf die Zelle Unicode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="75465-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75465-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="75465-109">Cell name:</span></span>  <br/> | <span data-ttu-id="75465-110">Fields. UICode [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="75465-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="75465-111">Wenn Sie einen Verweis auf die Zelle Unicode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="75465-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75465-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="75465-112">Section index:</span></span>  <br/> |<span data-ttu-id="75465-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="75465-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="75465-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="75465-114">Row index:</span></span>  <br/> |<span data-ttu-id="75465-115">**visRowField** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="75465-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="75465-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="75465-116">Cell index:</span></span>  <br/> |<span data-ttu-id="75465-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="75465-117">**visFieldUICode**</span></span> <br/> |
   

