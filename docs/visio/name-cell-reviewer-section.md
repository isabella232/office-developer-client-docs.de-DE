---
title: Zelle "Name" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Enthält den Namen des Bearbeiters eines Dokuments.
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797540"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="111f7-103">Name Cell (Reviewer Section)</span><span class="sxs-lookup"><span data-stu-id="111f7-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="111f7-104">Enthält den Namen des Bearbeiters eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="111f7-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="111f7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="111f7-105">Remarks</span></span>

 <span data-ttu-id="111f7-106">Dieser Wert entspricht standardmäßig der Name im Feld **Benutzername** auf der Registerkarte **Allgemein** im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf **Allgemein**).</span><span class="sxs-lookup"><span data-stu-id="111f7-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="111f7-107">Zum Abrufen eines Verweises auf die Zelle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="111f7-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="111f7-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="111f7-108">Cell name:</span></span>  <br/> | <span data-ttu-id="111f7-109">Reviewer.Name [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="111f7-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="111f7-110">Wenn Sie einen Bezug auf die Zelle Name aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="111f7-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="111f7-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="111f7-111">Section index:</span></span>  <br/> |<span data-ttu-id="111f7-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="111f7-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="111f7-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="111f7-113">Row index:</span></span>  <br/> |<span data-ttu-id="111f7-114">**VisRowReviewer** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="111f7-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="111f7-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="111f7-115">Cell index:</span></span>  <br/> |<span data-ttu-id="111f7-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="111f7-116">**visReviewerName**</span></span> <br/> |
   

