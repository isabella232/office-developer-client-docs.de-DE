---
title: Zelle "Bullet" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Bestimmt das Aufzählungszeichenformat.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796564"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="72635-103">Bullet Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="72635-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="72635-104">Bestimmt das Aufzählungszeichenformat.</span><span class="sxs-lookup"><span data-stu-id="72635-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="72635-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="72635-105">**Value**</span></span>|<span data-ttu-id="72635-106">**Formatvorlage für Bildaufzählungszeichen**</span><span class="sxs-lookup"><span data-stu-id="72635-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72635-107">0</span><span class="sxs-lookup"><span data-stu-id="72635-107">0</span></span>  <br/> |<span data-ttu-id="72635-108">Keine</span><span class="sxs-lookup"><span data-stu-id="72635-108">None</span></span>  <br/> |
|<span data-ttu-id="72635-109">1</span><span class="sxs-lookup"><span data-stu-id="72635-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="72635-110">2</span><span class="sxs-lookup"><span data-stu-id="72635-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="72635-111">3</span><span class="sxs-lookup"><span data-stu-id="72635-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="72635-112">4</span><span class="sxs-lookup"><span data-stu-id="72635-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="72635-113">5</span><span class="sxs-lookup"><span data-stu-id="72635-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="72635-114">6</span><span class="sxs-lookup"><span data-stu-id="72635-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="72635-115">7</span><span class="sxs-lookup"><span data-stu-id="72635-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="72635-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="72635-116">Section index:</span></span>  <br/> |<span data-ttu-id="72635-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="72635-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="72635-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="72635-118">Row index:</span></span>  <br/> |<span data-ttu-id="72635-119">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="72635-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="72635-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="72635-120">Cell index:</span></span>  <br/> |<span data-ttu-id="72635-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="72635-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72635-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72635-122">Remarks</span></span>

<span data-ttu-id="72635-123">Sie können auch den Wert dieser Zelle durch Festlegen der rechten Maustaste auf ein Shape klicken, auf **Format**, auf **Text**klicken und dann auf die Registerkarte **Aufzählungszeichen** zeigen.</span><span class="sxs-lookup"><span data-stu-id="72635-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="72635-124">Zum Abrufen eines Verweises auf die Zelle Bullet nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="72635-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72635-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="72635-125">Cell name:</span></span>  <br/> |<span data-ttu-id="72635-126">Para.Bullet [ *i* ] wobei *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="72635-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="72635-127">Wenn Sie einen Verweis auf die Zelle Bullet aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="72635-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

