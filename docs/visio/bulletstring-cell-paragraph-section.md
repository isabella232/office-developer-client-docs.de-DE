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
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796571"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="92ac6-103">BulletString Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="92ac6-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="92ac6-104">Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen.</span><span class="sxs-lookup"><span data-stu-id="92ac6-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="92ac6-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92ac6-105">Remarks</span></span>

<span data-ttu-id="92ac6-p101">Geben Sie die Formatvorlage in Form einer Zeichenfolge (eingeschlossen in Anführungszeichen) ein. Sie können beispielsweise die Zeichenfolge "ooo" eingeben.</span><span class="sxs-lookup"><span data-stu-id="92ac6-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="92ac6-108">Sie können auch den Wert dieser Zelle durch Festlegen der rechten Maustaste auf ein Shape klicken, auf **Format**, auf **Text**klicken und dann auf die Registerkarte **Aufzählungszeichen** zeigen.</span><span class="sxs-lookup"><span data-stu-id="92ac6-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="92ac6-109">Zum Abrufen eines Verweises auf die Zelle BulletString nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="92ac6-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92ac6-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="92ac6-110">Cell name:</span></span>  <br/> |<span data-ttu-id="92ac6-111">Para.BulletStr [ *i* ] wobei *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="92ac6-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="92ac6-112">Wenn Sie einen Verweis auf die Zelle BulletString aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="92ac6-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92ac6-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="92ac6-113">Section index:</span></span>  <br/> |<span data-ttu-id="92ac6-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="92ac6-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="92ac6-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="92ac6-115">Row index:</span></span>  <br/> |<span data-ttu-id="92ac6-116">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="92ac6-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="92ac6-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="92ac6-117">Cell index:</span></span>  <br/> |<span data-ttu-id="92ac6-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="92ac6-118">**visBulletString**</span></span> <br/> |
   

