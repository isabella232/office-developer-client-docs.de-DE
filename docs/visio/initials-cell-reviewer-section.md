---
title: Zelle "Initials" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Enthält die Initialen eines Dokumentbearbeiters.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797219"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="58fce-103">Initials Cell (Reviewer Section)</span><span class="sxs-lookup"><span data-stu-id="58fce-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="58fce-104">Enthält die Initialen eines Dokumentbearbeiters.</span><span class="sxs-lookup"><span data-stu-id="58fce-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58fce-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58fce-105">Remarks</span></span>

<span data-ttu-id="58fce-106">Standardwert sind die Initialen im Feld **Initialen** auf der Registerkarte **Allgemein** im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf **Allgemein** ).</span><span class="sxs-lookup"><span data-stu-id="58fce-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="58fce-107">Wenn Sie einen Verweis auf die Zelle Initials nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="58fce-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58fce-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="58fce-108">Cell name:</span></span>  <br/> | <span data-ttu-id="58fce-109">Reviewer.Initials [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="58fce-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="58fce-110">Wenn Sie einen Verweis auf die Zelle Initials aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="58fce-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58fce-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="58fce-111">Section index:</span></span>  <br/> |<span data-ttu-id="58fce-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="58fce-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="58fce-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="58fce-113">Row index:</span></span>  <br/> |<span data-ttu-id="58fce-114">**VisRowReviewer** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="58fce-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="58fce-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="58fce-115">Cell index:</span></span>  <br/> |<span data-ttu-id="58fce-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="58fce-116">**visReviewerInitials**</span></span> <br/> |
   

