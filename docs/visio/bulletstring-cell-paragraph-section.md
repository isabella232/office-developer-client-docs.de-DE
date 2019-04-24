---
title: Zelle "BulletString" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen.
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337562"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="6b3f4-103">Zelle "BulletString" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="6b3f4-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="6b3f4-104">Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen.</span><span class="sxs-lookup"><span data-stu-id="6b3f4-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6b3f4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b3f4-105">Remarks</span></span>

<span data-ttu-id="6b3f4-p101">Geben Sie die Formatvorlage in Form einer Zeichenfolge (eingeschlossen in Anführungszeichen) ein. Sie können beispielsweise die Zeichenfolge "ooo" eingeben.</span><span class="sxs-lookup"><span data-stu-id="6b3f4-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="6b3f4-108">Sie können den Wert für diese Zelle auch festlegen, indem Sie mit der rechten Maustaste auf ein Shape klicken, auf **Format** zeigen, auf **Text** klicken und dann die Registerkarte **Aufzählungszeichen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="6b3f4-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="6b3f4-109">Wenn Sie einen Verweis auf die Zelle Bullete aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6b3f4-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b3f4-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6b3f4-110">Cell name:</span></span>  <br/> |<span data-ttu-id="6b3f4-111">Abs. BulletStr [ *i* ] wobei *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="6b3f4-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="6b3f4-112">Wenn Sie einen Verweis auf die Zelle Bullete aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6b3f4-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b3f4-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6b3f4-113">Section index:</span></span>  <br/> |<span data-ttu-id="6b3f4-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="6b3f4-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="6b3f4-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6b3f4-115">Row index:</span></span>  <br/> |<span data-ttu-id="6b3f4-116">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="6b3f4-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="6b3f4-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6b3f4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6b3f4-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="6b3f4-118">**visBulletString**</span></span> <br/> |
   

