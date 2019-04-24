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
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335168"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="0144a-103">Zelle "Name" (Abschnitt "Reviewer")</span><span class="sxs-lookup"><span data-stu-id="0144a-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="0144a-104">Enthält den Namen des Bearbeiters eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0144a-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0144a-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0144a-105">Remarks</span></span>

 <span data-ttu-id="0144a-106">Dieser Wert ist standardmäßig der Name im Feld **Benutzername** auf der Registerkarte **Allgemein** des Dialogfelds **Visio-Optionen** (Klicken Sie auf die registerKarte **Datei** , klicken Sie auf **Optionen**und dann auf **Allgemein**).</span><span class="sxs-lookup"><span data-stu-id="0144a-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="0144a-107">Wenn Sie einen Verweis auf die Zelle Name aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0144a-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0144a-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0144a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="0144a-109">Reviewer.Name [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0144a-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0144a-110">Wenn Sie einen Verweis auf die Zelle Name aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0144a-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0144a-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0144a-111">Section index:</span></span>  <br/> |<span data-ttu-id="0144a-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="0144a-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="0144a-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0144a-113">Row index:</span></span>  <br/> |<span data-ttu-id="0144a-114">**visRowReviewer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0144a-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0144a-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0144a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0144a-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="0144a-116">**visReviewerName**</span></span> <br/> |
   

