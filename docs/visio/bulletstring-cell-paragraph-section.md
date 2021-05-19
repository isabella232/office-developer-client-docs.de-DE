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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409748"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="dcd59-103">Zelle "BulletString" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="dcd59-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="dcd59-104">Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen.</span><span class="sxs-lookup"><span data-stu-id="dcd59-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dcd59-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcd59-105">Remarks</span></span>

<span data-ttu-id="dcd59-p101">Geben Sie die Formatvorlage in Form einer Zeichenfolge (eingeschlossen in Anführungszeichen) ein. Sie können beispielsweise die Zeichenfolge "ooo" eingeben.</span><span class="sxs-lookup"><span data-stu-id="dcd59-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="dcd59-108">Sie können den Wert für diese Zelle auch festlegen, indem Sie mit der rechten Maustaste auf ein Shape klicken, auf **Format** zeigen, auf **Text** klicken und dann die Registerkarte **Aufzählungszeichen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="dcd59-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="dcd59-109">Verwenden Sie zum Erhalten eines Verweises auf die Zelle BulletString anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="dcd59-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcd59-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dcd59-110">Cell name:</span></span>  <br/> |<span data-ttu-id="dcd59-111">Para.BulletStr[ *i*  ] where  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="dcd59-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="dcd59-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle BulletString nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="dcd59-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcd59-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dcd59-113">Section index:</span></span>  <br/> |<span data-ttu-id="dcd59-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="dcd59-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="dcd59-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dcd59-115">Row index:</span></span>  <br/> |<span data-ttu-id="dcd59-116">**visRowParagraph**  +   *i* where *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="dcd59-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="dcd59-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dcd59-117">Cell index:</span></span>  <br/> |<span data-ttu-id="dcd59-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="dcd59-118">**visBulletString**</span></span> <br/> |
   

