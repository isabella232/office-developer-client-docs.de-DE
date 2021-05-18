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
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411505"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="9a190-103">Zelle "Initials" (Abschnitt "Reviewer")</span><span class="sxs-lookup"><span data-stu-id="9a190-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="9a190-104">Enthält die Initialen eines Dokumentbearbeiters.</span><span class="sxs-lookup"><span data-stu-id="9a190-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a190-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a190-105">Remarks</span></span>

<span data-ttu-id="9a190-106">Dieser Wert wird standardmäßig auf die Initialen  im Feld **Initialen** auf der  Registerkarte Allgemein im Dialogfeld **Visio-Optionen** festgelegt (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Optionen** und dann auf **Allgemein** ).</span><span class="sxs-lookup"><span data-stu-id="9a190-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="9a190-107">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Initialen anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="9a190-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a190-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9a190-108">Cell name:</span></span>  <br/> | <span data-ttu-id="9a190-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9a190-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9a190-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Initialen nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9a190-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a190-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9a190-111">Section index:</span></span>  <br/> |<span data-ttu-id="9a190-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="9a190-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="9a190-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9a190-113">Row index:</span></span>  <br/> |<span data-ttu-id="9a190-114">**visRowReviewer**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9a190-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9a190-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9a190-115">Cell index:</span></span>  <br/> |<span data-ttu-id="9a190-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="9a190-116">**visReviewerInitials**</span></span> <br/> |
   

