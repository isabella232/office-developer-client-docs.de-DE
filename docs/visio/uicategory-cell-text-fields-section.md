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
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434025"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="bae3a-103">Zelle "UICategory" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="bae3a-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="bae3a-104">Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="bae3a-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bae3a-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bae3a-105">Remarks</span></span>

<span data-ttu-id="bae3a-p101">Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie bezüglich der Abwärtskompatibilität diese Zelle, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="bae3a-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="bae3a-108">Wenn Sie einen Verweis auf die Zelle Zelle UICategory aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bae3a-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bae3a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bae3a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="bae3a-110">Fields. UICategory [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bae3a-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bae3a-111">Wenn Sie einen Verweis auf die Zelle Zelle UICategory aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bae3a-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bae3a-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bae3a-112">Section index:</span></span>  <br/> |<span data-ttu-id="bae3a-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="bae3a-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="bae3a-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bae3a-114">Row index:</span></span>  <br/> |<span data-ttu-id="bae3a-115">**visRowField** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bae3a-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bae3a-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bae3a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bae3a-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="bae3a-117">**visFieldUICategory**</span></span> <br/> |
   

