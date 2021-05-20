---
title: Zelle "BulletFont" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438463"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="8114a-103">Zelle "BulletFont" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="8114a-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="8114a-104">Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist.</span><span class="sxs-lookup"><span data-stu-id="8114a-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8114a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8114a-105">Remarks</span></span>

<span data-ttu-id="8114a-p101">Nummern von Schriftarten variieren entsprechend der im System installierten Schriftarten. Wenn der Wert 0 und eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge vorhanden ist, entspricht die verwendete Schriftart der Schriftart des ersten Zeichens des Absatzes.</span><span class="sxs-lookup"><span data-stu-id="8114a-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="8114a-108">Um einen Verweis auf die Zelle BulletFont anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="8114a-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8114a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8114a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="8114a-110">Para.BulletFont[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8114a-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8114a-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle BulletFont nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="8114a-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8114a-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8114a-112">Section index:</span></span>  <br/> |<span data-ttu-id="8114a-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8114a-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8114a-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8114a-114">Row index:</span></span>  <br/> |<span data-ttu-id="8114a-115">**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8114a-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8114a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8114a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="8114a-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="8114a-117">**visBulletFont**</span></span> <br/> |
   

