---
title: Zelle "ImgWidth" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797195"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="fcdf0-104">ImgWidth Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="fcdf0-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="fcdf0-p102">Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="fcdf0-107">= Breite \* 1</span><span class="sxs-lookup"><span data-stu-id="fcdf0-107">= Width \* 1</span></span>
  
<span data-ttu-id="fcdf0-108">Beim Zuschneiden des Objekts ändert sich der Faktor, mit dem die Breite multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="fcdf0-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fcdf0-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fcdf0-109">Remarks</span></span>

<span data-ttu-id="fcdf0-110">Wenn Sie einen Verweis auf die Zelle ImgWidth aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fcdf0-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fcdf0-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="fcdf0-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="fcdf0-113">Wenn Sie einen Verweis auf die Zelle ImgWidth aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fcdf0-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-114">Section index:</span></span>  <br/> |<span data-ttu-id="fcdf0-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fcdf0-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fcdf0-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-116">Row index:</span></span>  <br/> |<span data-ttu-id="fcdf0-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="fcdf0-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="fcdf0-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fcdf0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fcdf0-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="fcdf0-119">**visFrgnImgWidth**</span></span> <br/> |
   

