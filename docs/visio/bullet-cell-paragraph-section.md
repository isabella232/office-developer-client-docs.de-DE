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
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="7d9b5-103">Bullet Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="7d9b5-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="7d9b5-104">Bestimmt das Aufzählungszeichenformat.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="7d9b5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7d9b5-105">**Value**</span></span>|<span data-ttu-id="7d9b5-106">**Formatvorlage für Bildaufzählungszeichen**</span><span class="sxs-lookup"><span data-stu-id="7d9b5-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d9b5-107">0</span><span class="sxs-lookup"><span data-stu-id="7d9b5-107">0</span></span>  <br/> |<span data-ttu-id="7d9b5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7d9b5-108">None</span></span>  <br/> |
|<span data-ttu-id="7d9b5-109">1</span><span class="sxs-lookup"><span data-stu-id="7d9b5-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="7d9b5-110">2</span><span class="sxs-lookup"><span data-stu-id="7d9b5-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="7d9b5-111">3</span><span class="sxs-lookup"><span data-stu-id="7d9b5-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="7d9b5-112">4</span><span class="sxs-lookup"><span data-stu-id="7d9b5-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="7d9b5-113">5</span><span class="sxs-lookup"><span data-stu-id="7d9b5-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="7d9b5-114">6</span><span class="sxs-lookup"><span data-stu-id="7d9b5-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="7d9b5-115">7</span><span class="sxs-lookup"><span data-stu-id="7d9b5-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="7d9b5-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-116">Section index:</span></span>  <br/> |<span data-ttu-id="7d9b5-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7d9b5-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="7d9b5-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-118">Row index:</span></span>  <br/> |<span data-ttu-id="7d9b5-119">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="7d9b5-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="7d9b5-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7d9b5-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="7d9b5-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d9b5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d9b5-122">Remarks</span></span>

<span data-ttu-id="7d9b5-123">Sie können den Wert für diese Zelle auch festlegen, indem Sie mit der rechten Maustaste auf ein Shape klicken, auf **Format** zeigen, auf **Text** klicken und dann die Registerkarte **Aufzählungszeichen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="7d9b5-124">Wenn Sie einen Verweis auf die Zelle Bullet aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d9b5-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-125">Cell name:</span></span>  <br/> |<span data-ttu-id="7d9b5-126">Para.Bullet [ *i* ] wobei *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="7d9b5-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="7d9b5-127">Wenn Sie einen Verweis auf die Zelle Bullet aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

