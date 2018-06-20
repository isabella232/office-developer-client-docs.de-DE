---
title: Zelle "ImgHeight" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797197"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="7d527-104">Zelle "ImgHeight" (Abschnitt "Foreign Image Info")</span><span class="sxs-lookup"><span data-stu-id="7d527-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="7d527-p102">Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="7d527-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="7d527-107">= Höhe \* 1</span><span class="sxs-lookup"><span data-stu-id="7d527-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d527-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d527-108">Remarks</span></span>

<span data-ttu-id="7d527-109">Wenn Sie einen Verweis auf die Zelle ImgHeight nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7d527-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d527-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7d527-110">Cell name:</span></span>  <br/> | <span data-ttu-id="7d527-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="7d527-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="7d527-112">Wenn Sie einen Verweis auf die Zelle ImgHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7d527-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d527-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7d527-113">Section index:</span></span>  <br/> |<span data-ttu-id="7d527-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7d527-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7d527-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7d527-115">Row index:</span></span>  <br/> |<span data-ttu-id="7d527-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="7d527-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="7d527-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7d527-117">Cell index:</span></span>  <br/> |<span data-ttu-id="7d527-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="7d527-118">**visFrgnImgHeight**</span></span> <br/> |
   

