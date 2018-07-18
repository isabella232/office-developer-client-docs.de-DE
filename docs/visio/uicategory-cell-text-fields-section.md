---
title: Zelle "UICategory" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.
ms.openlocfilehash: fc060ac1533732749d10e1855dc3841602051520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798345"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="fd3bd-103">UICategory Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="fd3bd-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="fd3bd-104">Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="fd3bd-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd3bd-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd3bd-105">Remarks</span></span>

<span data-ttu-id="fd3bd-p101">Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie bezüglich der Abwärtskompatibilität diese Zelle, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="fd3bd-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="fd3bd-108">Wenn Sie einen Verweis auf die Zelle UICategory aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fd3bd-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd3bd-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fd3bd-109">Cell name:</span></span>  <br/> | <span data-ttu-id="fd3bd-110">Fields.UICat [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fd3bd-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fd3bd-111">Wenn Sie einen Verweis auf die Zelle UICategory aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="fd3bd-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd3bd-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fd3bd-112">Section index:</span></span>  <br/> |<span data-ttu-id="fd3bd-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="fd3bd-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="fd3bd-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fd3bd-114">Row index:</span></span>  <br/> |<span data-ttu-id="fd3bd-115">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fd3bd-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fd3bd-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fd3bd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fd3bd-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="fd3bd-117">**visFieldUICategory**</span></span> <br/> |
   

