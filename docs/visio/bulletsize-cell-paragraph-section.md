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
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405422"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="cf1a4-103">Zelle "BulletSize" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="cf1a4-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="cf1a4-104">Gibt die Größe eines Aufzählungszeichens an.</span><span class="sxs-lookup"><span data-stu-id="cf1a4-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf1a4-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf1a4-105">Remarks</span></span>

<span data-ttu-id="cf1a4-106">Dieser Wert kann sowohl für vordefinierte als auch für benutzerdefinierte Aufzählungszeichen als Prozentsatz oder als spezifischer Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf1a4-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="cf1a4-107">Wenn der Wert null (0) ist, hat das Aufzählungszeichen dieselbe Schriftgröße wie das erste Zeichen im Absatz.</span><span class="sxs-lookup"><span data-stu-id="cf1a4-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="cf1a4-108">Wenn der Wert ein Prozentsatz ist, erhält das Aufzählungszeichen einen Schriftgrad, der prozentual vom Schriftgrad des ersten Zeichens im Absatz abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="cf1a4-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="cf1a4-109">Negative Zahlen werden als Prozentsätze behandelt.</span><span class="sxs-lookup"><span data-stu-id="cf1a4-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="cf1a4-110">Um einen Verweis auf die Zelle BulletSize anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="cf1a4-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf1a4-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cf1a4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="cf1a4-112">Para.BulletFontSize[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cf1a4-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cf1a4-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BulletSize-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="cf1a4-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf1a4-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cf1a4-114">Section index:</span></span>  <br/> |<span data-ttu-id="cf1a4-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="cf1a4-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="cf1a4-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cf1a4-116">Row index:</span></span>  <br/> |<span data-ttu-id="cf1a4-117">**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cf1a4-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cf1a4-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cf1a4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="cf1a4-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="cf1a4-119">**visBulletFontSize**</span></span> <br/> |
   

