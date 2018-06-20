---
title: Zelle "BulletSize" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Gibt die Größe eines Aufzählungszeichens an.
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796545"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="7b528-103">BulletSize Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="7b528-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="7b528-104">Gibt die Größe eines Aufzählungszeichens an.</span><span class="sxs-lookup"><span data-stu-id="7b528-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7b528-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b528-105">Remarks</span></span>

<span data-ttu-id="7b528-106">Dieser Wert kann sowohl für vordefinierte als auch für benutzerdefinierte Aufzählungszeichen als Prozentsatz oder als spezifischer Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b528-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="7b528-107">Wenn der Wert NULL (0) ist, wird das Aufzählungszeichen die gleiche Schriftgröße wie das erste Zeichen im Absatz.</span><span class="sxs-lookup"><span data-stu-id="7b528-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="7b528-108">Wenn der Wert ein Prozentsatz ist, wird das Aufzählungszeichen als Prozentsatz der Schriftgrad des ersten Zeichens im Absatz angepasst.</span><span class="sxs-lookup"><span data-stu-id="7b528-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="7b528-109">Negative Zahlen werden als Prozentsätze behandelt.</span><span class="sxs-lookup"><span data-stu-id="7b528-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="7b528-110">Wenn Sie einen Verweis auf die Zelle BulletSize nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7b528-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b528-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7b528-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7b528-112">Para.BulletFontSize [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7b528-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7b528-113">Wenn Sie einen Verweis auf die Zelle BulletSize aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7b528-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b528-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7b528-114">Section index:</span></span>  <br/> |<span data-ttu-id="7b528-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7b528-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="7b528-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7b528-116">Row index:</span></span>  <br/> |<span data-ttu-id="7b528-117">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7b528-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7b528-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7b528-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7b528-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="7b528-119">**visBulletFontSize**</span></span> <br/> |
   

